# PaperBait

PaperBait app is <br/>

This app has two separate modules<br/>

Website written in php 7.4 js and using bootstrap 5<br/> a
Game written in CPP using SDL2 compiled to js with Emscripten<br/>

## How this works?

Application is using database to for storageing data, and php for transactions.
Some PHP files are used by ajax from game, these scripts allow to read and save data eg. money and gamestate.
Website is using OCR for reading receipe values and then counts points for players

## How to install* ?
Instruction for debian systems

1. Already compiled code:<br/>
    - Install required components 
    ```
      sudo apt install tesseract-ocr
      sudo apt install php-xmlrpc
      sudo apt install php-mysql
      sudo apt install php-common
      sudo apt install php-imagick

    ```
    - Install Language component for ocr eg.
    ```
    sudo apt install tesseract-ocr-pol
    ```
    - Prepare database<br/>
    ```
    sudo apt install mariadb-server
    ```
        - Log into mysql
        ```
        sudo mysql -p
        ```
        - create new database
        ```
        CREATE database db_paperbait;
        CREATE USER paperbait IDENTYFIED BY 'password';
        GRANT ALL PRIVILEGES ON db_paperbait.* to paperbait;
        ```
    - Copy all content from website to public_html<br/>
    - Insert username, password, database name, host into connector.php<br/>
2. Compile code on my own<br/>
    - All previous steps<br/>
    - Install SDL modules (Base, audio, ttf etc.)<br/>
    ```
    sudo apt install libsdl2-*
    ```
    - Install emscripten [from here](https://emscripten.org)<br/>
    - Compile with custom options or via compile.sh inside cpp project<br/>
    

### How to change in game item value
-Open file CarouselMenu.cpp<br/>
-Find method init_food or init_fishes<br/>
-Change values as you desire<br/>
-Compile Game and move to public_html<br/>
