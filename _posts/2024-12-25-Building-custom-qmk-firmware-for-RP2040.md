---
layout: post
date: 2024-12-25
tags:
  - qmk
---
This is how I personally managed to get a binary file adequate for the RP2040 MCU in my ferris sweep setup

Clone qmk repo
`git clone https://github.com/qmk/qmk_firmware.git`
Cd to the repo
Build the dev shell on nixOs
`nix-shell shell.nix`
update submodules
`git submodule update --init --recursived`

go to https://config.qmk.fm/#/ferris/sweep/LAYOUT_split_3x5_2
modify your keymap. 
Download your JSON with changes
(in this example i am modifying my ferris sweep to hold a layer with just the left hand keyboard holding just the letter keys so i dont have to deal with layers while gaming)

copy said json into your corresponding subfolder (in my case i copied it to the keyboards/ferris/sweep/keymaps/gamemod)(i had to mkdir gamemod)

name it keymap.json

compile your keymap
`qmk compile -c -kb ferris/sweep -km gamemod -e CONVERT_TO=promicro_rp2040`


once it is done compiling, you can find it in the root of qmk_firmware. Then simply flash your microcontrollers and enjoy!!!!