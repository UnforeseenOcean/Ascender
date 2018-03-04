# Ascender
Server emulator for Ascend: Hand of Kul

## Introduction
This is currently a information sharing page/repository for the game Ascend: Hand of Kul.

Our (my?) goal is to create a local server for the game, since the official server has closed down in 2016.

Think of Mooege or Vindictus Offline (I think it was called like that? Correct me if I'm wrong).

I apologize if this repo made you run to the toilet with sheer volume of uneducated guessworks!

## Files
`LICENSE`: License info. This repo is licenced under LGPL-3.0.

`MEMDUMP_TRUNCATED.TXT`: A memory string dump of the game. This reveals some slightly mangled scripts used by the game, totally unencrypted/decompressed. I haven't been able to locate the magic word for each file, so direct decomp/decrypt is not possible yet for me.

`PROTOCOL.md`: Documentation on the protocols used by this game. Sadly, I need to figure out how to make the game go past the error screen in order to update this documentation.

`README.md`: This file!

`WHATWEKNOW.md`: Document detailing what I have found over the time using various methods, such as debuggers, memory dumps, static analysis (surface level, unfortunately...)

`res.sacb.idx`: A file index found inside the data blob. Use the BMS Script included inside `WHATWEKNOW.md` to unpack the `res.sacb` file.

## Credits
- LiveOverflow - Awesome guy, I used some of his tactics to pull some info out of the "post-mortem flight-recorder data mess".
