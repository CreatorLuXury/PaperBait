# PaperBait

PaperBait app is 

This app has two separate modules

Website written in php/js
Game written in CPP using SDL2 compiled to js with Emscripten

## How this works?

Application is using database to for storageing data, and php for transactions.
Some PHP files are used by ajax from game, these scripts allow to read and save data eg. money and gamestate.
Website is using OCR for reading receipe values and then counts points for players

## How to install?

  1.Already compiled code:
    Prepare database
    Copy all content from website to public_html
    Insert username, password, database name, host into connector.php
  2.Compile code on my own
    All previous steps
    Install SDL modules (Base, audio, ttf etc.)
    Install emscripten [from here](https://emscripten.org)
    compile with custom options or via compile.sh inside cpp project
    

### How to change in game item value
Open file CarouselMenu.cpp
Find method init_food or init_fishes
Change values as you desire
Compile Game and move to public_html
