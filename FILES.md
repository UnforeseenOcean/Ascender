# About file format
This document describes what I currently know about this game's files.

## `.*b` format
Name suggests `bzip` compression, however it's most likely `zlib` compression.

## `.nutb` file
This is very likely Squirrel, a game-focused programming language. http://squirrel-lang.org/

The script file has a weird header, which fits into the `sigb` format. It tells the game engine what file should be loaded for each script.

The beginning of the game is contained within `/gui/scripts/fuisquirrellinkage.nutb`

## `.sigb` file
This one looks like a bunch of instructions on what file to use for each event/action/script. I don't know what's up with this file, but it has a bunch of unrecognizable characters.

Update: This looks like a table file.

## `.tabb` file
Contextually this is a table file, containing internal values of the game, such as all the valid values from the server, all the items, all the weapons and so on. Unknown format. If I manage to decode this somehow, I could be able to find what value the game wants from the server.

## `.tgab` and `.pngb` file
This one is a real head-scratcher. It does not fit into any type of compression I know of. It has no valid header too. I'm still investigating about this.

## `.swfb` file
This is here because of Iggy, a Flash-based UI solution. I was unable to make this work either; It has some weird header I don't know of.


(I can only imagine Permanull's face when I put my guessworks on GitHub...)
