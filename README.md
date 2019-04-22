# Ascender
Server emulator for Ascend: Hand of Kul

Check our Discord server for updates, info and discussion (and also help us there)

Also thank Permanull while you are at it, he really deserves it.

https://discord.gg/PpgHEB8


## Introduction
This is currently a information sharing page/repository for the game Ascend: Hand of Kul.

The goal is to create a local server for the game, since the official server has closed down in 2016.

(Mad props to Permanull, he definitely knows what he is doing unlike me :pensive:)

p.s. Dear developers at Signal Studios, if you are reading this and loved this game and want to bring it back, please consider helping us. Thank you.

## How to download the game
1. Install Steam.
2. Register or log into your account.
3. Follow this link: steam://install/233630/
4. You're done! This requires at least 2GB of hard disk space.

## Files
`LICENSE`: License info. This repo is licenced under LGPL-3.0.

`Updates.md`: This is the update log. I'll try my best to keep track of the updates, but Permanull is really talented and the progress is very fast, so it might be outdated or less-than-ideal.

`MEMDUMP_TRUNCATED.TXT`: A memory string dump of the game. This reveals some slightly mangled scripts used by the game, totally unencrypted/decompressed. I haven't been able to locate the magic word for each file, so direct decomp/decrypt is not possible yet for me.

`PROTOCOL.md`: Documentation on the protocols used by this game. Sadly, I need to figure out how to make the game go past the error screen in order to update this documentation.

`README.md`: This file!

`WHATWEKNOW.md`: Document detailing what I have found over the time using various methods, such as debuggers, memory dumps, static analysis (surface level, unfortunately...)

`res.sacb.idx`: A file index found inside the data blob. Use the QuickBMS Script included inside `WHATWEKNOW.md` to unpack the `res.sacb` file.

`FILES.MD`: Information on this game's files.

`ServerComm.md`: A work-in-process writeup of this game's inner workings, specifically the server communication portion. Thank you Permanull!

## Credits
- **permanull - The Boss (he's programming everything and I can't thank him enough)** :heart: :heart: :heart:
- LiveOverflow - Awesome guy, I used some of his tactics to pull some info out of the "post-mortem flight-recorder data mess".
- Luigi Auriemma - Maker of QuickBMS.
- XeNTaX - I reused the unpacking code for Toy Soldiers (which had same data blob structure) to unpack data file. Original script can be found [on this link.](http://forum.xentax.com/viewtopic.php?f=10&t=8860)
- swuforce - Creator of aforementioned QuickBMS script. I borrowed their script from their forum post.

## Manifesto
> Despite my lack of skills I wanted to show people that this game is really something, that the game deserves a second chance, that this game could serve as a reminder for its innovation and as a motivation for future developers. Maybe one day someone comes across this game on the archives far into the future, maybe after Steam closes down and none of people who have worked on this game and this project remains, plays it, gets inspired and starts making games to instill creativity and imagination to the future generations to come. That is my hope and the reason I started this project. I wanted to inspire, entertain and motivate people to be better. - *UnforeseenOcean*

## DISCLAIMER
This repository and all of its contents are provided "as-is" without any warranty. By downloading or using any part of this repository you accept any and all risk and responsibility associated with the use of binary file and/or code snippets.
