# What We Know

## Server addresses
`prod.api.ascendgame.com`

`gds4.steampowered.com`

`1.214.68.2` (Unconfirmed)

## Technologies used
libogg.dll - Ogg Vorbis by Xiph.org

libtheora.dll - Theora by Xiph.org

libvorbis.dll - Vorbis by Xiph.org

iggy_w32.dll - Iggy by RAD Game Tools

Bzip/Gzip/LZMA

Deflate/Inflate (Inflate library used in-game)

zlib

OGG Video

SharpDX - SharpDX by Alexandre Mutel

AudioKinetic Wwise RIFF 

## Game Engine
Uses engine used in Toy Soldiers (and similar future PC releases from Signal Studios)

## .\*b format
`.oggb` and such files have weird file structure.
`.tgab` files have static 70(16) bytes of data and seems to be regular Targa image files.
`.nutb` files have F0(16) bytes of junk data.
`.xmlb` files have this header: `(4 byte header)!SigB!(02 00)(4 byte header)(80 bytes of null)`

### .BNK and .WEM files
Using Wwise Audio Bank Extractor will extract some sort of audio data with `.wav` extension, but it's not playable yet. Seems to be either headless file or is using some sort of external compression.

## QuickBMS script for unpacking data file (use command-line mode, not GUI mode)
```
goto 0x68
get FILES long
math OFF = 0x78
for i = 0 < FILES
goto OFF
get NAMEOFF THREEBYTE
math NAMEOFF -= 4
get DUMMY byte
get NAMESIZE long
get UNK1 long
get UNK2 long
get OFFSET long
get ZSIZE long
get SIZE long
getdstring DUMMY 0x1c
savepos OFF
goto NAMEOFF
getdstring NAME NAMESIZE
if SIZE == ZSIZE
log NAME OFFSET SIZE
else
clog NAME OFFSET ZSIZE SIZE
endif
next i
```
Command: `quickbms.exe (script file name) res.sacb (destination folder)`
