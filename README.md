# PaperBait

PaperBait app is <br/>

This app has two separate modules<br/>

Website written in php/js<br/>
Game written in CPP using SDL2 compiled to js with Emscripten<br/>

## How this works?

Application is using database to for storageing data, and php for transactions.
Some PHP files are used by ajax from game, these scripts allow to read and save data eg. money and gamestate.
Website is using OCR for reading receipe values and then counts points for players

## How to install?

1. Already compiled code:<br/>
    - Prepare database<br/>
    - Copy all content from website to public_html<br/>
    - Insert username, password, database name, host into connector.php<br/>
2. Compile code on my own<br/>
    - All previous steps<br/>
    - Install SDL modules (Base, audio, ttf etc.)<br/>
    - Install emscripten [from here](https://emscripten.org)<br/>
    - Compile with custom options or via compile.sh inside cpp project<br/>
    

### How to change in game item value
-Open file CarouselMenu.cpp<br/>
-Find method init_food or init_fishes<br/>
-Change values as you desire<br/>
-Compile Game and move to public_html<br/>
