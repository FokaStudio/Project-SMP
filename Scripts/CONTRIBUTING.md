### Table of Contents
- [Contributing](#contributing)
- [Copyright Notice](#copyright-notice)
- [Code Conventions](#code-conventions)

# Contributing
![Lines of code](https://img.shields.io/tokei/lines/github/Project-SMP/Project-SMP?color=1&label=Lines%20of%20code&logo=Visual%20Studio%20Code&logoColor=blue&style=for-the-badge)


As I have stated in [README.md](README.md), I use *Skript* for everything related to coding in there.

I would be grateful if you would do so too! I accept *Denizen* scripts and actual plugins *(if you are smart)* too though, so no worries!

# Copyright Notice
![License](https://img.shields.io/github/license/Project-SMP/Project-SMP?logo=gnu&logoColor=orange&style=for-the-badge)

This repo and all work inside it is licensed under [**FokaStudio's Very Own DO WHATEVER THE FUCK YOU WANT WITH THIS License**](../LICENSE), meaning that:
1. You are free to download the work created here and use it for yourself *(on both private and public servers)*
2. You must not remove the copyright and ownership notices 
3. You can redistribute the work if you are sticking to certain conditions
4. You must open source the code when you redistribute it
5. If you are contributing - you have to license your work under the same license and put this on top of the file:
   
    ```t
    #
    # Copyright 2021 - FokaStudio
    # Contributed to Project: SMP by <contributors>
    #
    # https://github.com/Project-SMP
    #
    ```
   Replace `<contributors>` with names of all people who have put some effort in making of the code.

6. Any script made for the server must be free. Contents of this repo will always be accesible to everyone (unless Foka takes their rights away)

# Code Conventions
1. All work must be properly commented for purpose of letting everyone know what a particular part of the script is doing
   1. Comments can be added after the initial PR with the contributed material
   2. Commenting:
        ```
        # single hastag - least important stuff
        #! hastag and exclamation mark - important stuff
        #!! hastag and 2 exclamation marks - additional info
        ```
        Follow this format, because of VSC's formatting of comments
2. You should put a list that is EXACTLY LIKE this after the copyright notice:

    ```t
    #
    # Coded by: <contributors>
    # Original by: <author>
    # Addons required: <addons>
    # Other plugins: <plugins>
    ```
    Replace values in `<>` with respective things:

    `<contributors>` = people who have coded the script (e.g. 'FokaStudio', 'RandomPlayerNameHere', etc.)
    `<author>` = if it is a port or if the script is based on another script, this thing should be set to the original author (e.g. `RandomPlayerNameHere', 'FokaStudio', etc.)
    `<addons>` = required Skript addons (e.g. 'skript-reflect', 'SkBee', 'SkQuery')
    `<plugins>` = Other plugins required to make the code run (e.g. 'AureliumSkills', 'NBTAPI')

3. If you wish to use **skript-reflect** make sure that:
   1. You follow [*skript-reflect's code conventions*](https://tpgamesnl.gitbook.io/skript-reflect/code-conventions)
   2. Don't overuse reflections, e.g. if have to use `event.getBlock()` several times, make it more like this:
        ```applescript
        set {_block_} to event.getBlock()
        {_block_}.doStuff1()
        {_block_}.doMoreStuff1()
        {_block_}.doEvenMoreStuff1()
        ```
        ***Too many reflections lag terribly and slow parse time. Do it like this if you want to use many of the same reflections***
    1. Don't use reflections for something that is possible with vanilla Skript or any of the Addons! Better read [documentation](https://skripthub.net/docs/) first!
   