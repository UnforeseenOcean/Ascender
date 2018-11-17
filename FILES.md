# About file format
This document describes what I currently know about this game's files.

## `.*b` format
Name suggests `bzip` compression, however it's most likely `zlib` compression.

## `.nutb` file
This is very likely Squirrel, a game-focused programming language. http://squirrel-lang.org/

## `.tgab` and `.pngb` file
This one is a real head-scratcher. It does not fit into any type of compression I know of. It has no valid header too. I'm still investigating about this.

## `.swfb` file
This is here because of Iggy, a Flash-based UI solution. I was unable to make this work either; It has some weird header I don't know of.

