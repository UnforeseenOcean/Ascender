# Ascender
Server emulator for Ascend: Hand of Kul

## Introduction
This is currently a information sharing page/repository for the game Ascend: Hand of Kul.

~~Our~~ The goal is to create a local server for the game, since the official server has closed down in 2016.

(Mad props to Permanull, they definitely know what they are doing unlike me :pensive:)

Think of Mooege or Vindictus Offline (I think it was called like that? Correct me if I'm wrong).

I apologize if this repo made you run to the toilet with sheer volume of uneducated guessworks!

p.s. Dear developers at Signal Studios, if you are reading this and loved this game and want to bring it back, please consider helping us. Thank you.

## How to download the game
1. Install Steam.
2. Register or log into your account.
3. Follow this link: steam://install/233630/
4. You're done! This requires at least 2GB of hard disk space.

### Want only the executable?
Go to https://drive.google.com/file/d/1f7nQuWxw2IqRRlWysPzU0b-OOW8SLb6N/view?usp=sharing

This file will be deleted immediately upon request.

## Files
`LICENSE`: License info. This repo is licenced under LGPL-3.0.

`MEMDUMP_TRUNCATED.TXT`: A memory string dump of the game. This reveals some slightly mangled scripts used by the game, totally unencrypted/decompressed. I haven't been able to locate the magic word for each file, so direct decomp/decrypt is not possible yet for me.

`PROTOCOL.md`: Documentation on the protocols used by this game. Sadly, I need to figure out how to make the game go past the error screen in order to update this documentation.

`README.md`: This file!

`WHATWEKNOW.md`: Document detailing what I have found over the time using various methods, such as debuggers, memory dumps, static analysis (surface level, unfortunately...)

`res.sacb.idx`: A file index found inside the data blob. Use the QuickBMS Script included inside `WHATWEKNOW.md` to unpack the `res.sacb` file.

`FILES.MD`: Information on this game's files.

`ServerComm.md`: A work-in-process writeup of this game's inner workings, specifically the server communication portion. Thank you Permanull!

## Credits
- LiveOverflow - Awesome guy, I used some of his tactics to pull some info out of the "post-mortem flight-recorder data mess".
- Luigi Auriemma - Maker of QuickBMS.
- XeNTaX - I reused the unpacking code for Toy Soldiers (which had same data blob structure) to unpack data file. Original script can be found [on this link.](http://forum.xentax.com/viewtopic.php?f=10&t=8860)
- swuforce - Creator of aforementioned QuickBMS script. I borrowed their script from their forum post.
- **permanull - Tremendous helper from Reddit! Thanks a lot for solving login error!** :heart: :heart: :heart:

## DISCLAIMER
The files from the game are only provided for reference use only. To protect the intellectual property of original developers and companies, only the main executable will be provided, and provided executable will be removed upon request from the developers. I highly recommend downloading the entire game through official sources (Steam).
