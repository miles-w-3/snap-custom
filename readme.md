# SNAP

![SNAP](https://nullbits.co/static/img/snap10.jpg)


## Fork
> Fork of [snap qmk firmware](https://github.com/nullbitsco/snap) to customize and add personal layouts 

### Installation 
1. Follow the instructions to set up [qmk environment](https://docs.qmk.fm/#/getting_started_build_tools)
2. Clone this repo and add it to the keyboards folder
    - If on an environemnt that supports symlinks, you can link what you cloned to the original repo: 
    - This lets you manage the repo separately
    - On mac, within the qmk_firmware keyboard folder for nullbitsco (default `~/qmk_firmware/keyboards/nullbitsco`): 
    - `ln -a /path/to/this/repo folder_name`
    - For exmample, `ln -s ~/repos/projects/snap-custom snap` creates a `snap` folder in the `nullbitsco` folder that is tied to this repo 

### Build Custom
Once the folder has been added or symlinked, you can build the firmware you need using the qmk firmware Makefile
From the `qmk_firmware` dir:
`make nullbitsco/your_folder:desired_keymap`
- Where `desired_layout` is a folder in the `keymmaps` dir
- `make nullbitsco/snap:kilo`


## Original

A unique, tweakable split 75% keyboard kit built by nullbits. [More info at nullbits.co](https://nullbits.co/nibble/)

* Keyboard Maintainer: [Jay Greco](https://github.com/jaygreco)
* Hardware Supported: SNAP Rev1, Pro Micro comaptible MCUs.
* Hardware Availability: [nullbits.co](https://nullbits.co/)

Note: If you are seeing issues with MacOS and keyboard hangs after sleep, make sure `NO_USB_STARTUP_CHECK = yes` is set in your rules.mk.

Adds experimental "Remote Keyboard" functionality, which forwards keystrokes from an external macropad, keyboard, or numpad over UART/TRRS, removing the need for an additional USB connection. 

Make example for this keyboard (after setting up your build environment):

    make nullbitsco/snap:default

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).
