### Initial Communication

The game appears to first attempt to make a request to the following url:

https://prod.api.ascendgame.com/game/auth/steam?x=0&AuthTicket=XXXX&ClientVersion=1%2E1%2E0%2E3

The game does implement SSL and Certificate pinning but I was able to remove the SSL requirement with some patches in the executable, and log the headers being sent among other things.

### Request Headers
    [HTTP_HOST] => prod.api.ascendgame.com:443
    [HTTP_SEQUENCE_ID] => -1
    [HTTP_SIGNING_KEY] => 1
    [HTTP_CHECKSUM] => F4ACB721684B256A
    [HTTP_USER_AGENT] => Ascend

### Response
I haven't been able to determine what it's looking for in response to this, and returning random data still results in the game claiming the connection to the server was lost, I'm beginning to wonder if the web side is supposed to leave the connection open and stream data over time in the same socket/connection, I haven't tried leaving it half-open and simply not returning any data.


#### Offsets 
The following offsets are related to this behavior
**Game.exe+0x500181** - I call this "CheckWebConnection" it seems to perform various actions in a loop in order to actually build the data not only to make the request but in order to receive the response, within this it makes use of an Asynchronous implementation of the WININET library.

**Game.exe+0x00501ED1** - This is the actual function responsible for building the URL and parameters to be requested, it may do slightly more I haven't fully stepped through it. It appears to consist of a jump table based on an action which is defined by the first byte within the this pointer.

**Game.exe+0x00500293** - This is the offset to the call for the disconnected message that's displayed on the screen, the actual function pushes an event to the 'canvas' which the UI libraries than later react to by displaying the disconeccted message box.

The current running theory is that the game will attempt to make 4 attempts 1-5 (non 0 indexed) in order to 'connect' to the web service and after the 4th attempt it will display this faliure message.

If you review IDA's psuedo code you can see this behavior:
![IDA Fail message](https://i.gyazo.com/6b7c0d7df02962a8c4fc1d7f1db8813e.png)

Where **v1[0x0C827]** is compared against being reater than or equal to 5, you'll notice later on it's actually incremented as well,
Basically when the function at *0x00501ED1* returns, the value it returns with is compared and this function either continues to execute or it does not...

My guess is this routine is supposed to stop executing at the point that the connection was succesfull and never actually increment that value to or above 5.

The odd thing to mention there being the other potential URLs related to the game within the same routine, the odd thing is this function also appears to be responsible for building the request in the first place. Or it re-builds the same request each time.

