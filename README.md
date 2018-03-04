# Ascender
Server emulator for Ascend: Hand of Kul

## Introduction
This is currently a information sharing page/repository for the game Ascend: Hand of Kul.

Our (my?) goal is to create a local server for the game, since the official server has closed down in 2016.

Think of Mooege or Vindictus Offline (I think it was called like that? Correct me if I'm wrong).

I apologize if this repo made you run to the toilet with sheer volume of uneducated guessworks!

## How to download the game
1. Install Steam.
2. Register or log into your account.
3. Follow this link: steam://install/233630/
4. You're done! This requires at least 2GB of hard disk space.
## Files
`LICENSE`: License info. This repo is licenced under LGPL-3.0.

`MEMDUMP_TRUNCATED.TXT`: A memory string dump of the game. This reveals some slightly mangled scripts used by the game, totally unencrypted/decompressed. I haven't been able to locate the magic word for each file, so direct decomp/decrypt is not possible yet for me.

`PROTOCOL.md`: Documentation on the protocols used by this game. Sadly, I need to figure out how to make the game go past the error screen in order to update this documentation.

`README.md`: This file!

`WHATWEKNOW.md`: Document detailing what I have found over the time using various methods, such as debuggers, memory dumps, static analysis (surface level, unfortunately...)

`res.sacb.idx`: A file index found inside the data blob. Use the QuickBMS Script included inside `WHATWEKNOW.md` to unpack the `res.sacb` file.

## Credits
- LiveOverflow - Awesome guy, I used some of his tactics to pull some info out of the "post-mortem flight-recorder data mess".
- Luigi Auriemma - Maker of QuickBMS.
- XeNTaX - I reused the unpacking code for Toy Soldiers (which had same data blob structure) to unpack data file. Original script can be found [on this link.](http://forum.xentax.com/viewtopic.php?f=10&t=8860)
- swuforce - Creator of aforementioned QuickBMS script. I borrowed their script from their forum post.

## DISCLAIMER
The files from the game are only provided for reference use only. To protect the intellectual property of original developers and companies, only the main executable will be provided, and provided executable will be removed upon request from the developers. I highly recommend downloading the entire game through official sources (Steam).
