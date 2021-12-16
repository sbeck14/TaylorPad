# TaylorPad

<div align="center"><img src="./TaylorPad.png" width="300px"></div>

TaylorPad is a simple DIY macropad with a rotary encoder and 6 mechanical switches.

It is inspired by the [CapsUnlocked CU7](https://caps-unlocked.com/group-buy-cu7-round-2-5/), an very, very nice compact macropad made from custom-machined aluminum.

This is a handwired macropad with a 3D printed case. You can get as fancy or as 3D printed as you wish with the encoder knob and the keycaps.

## Example Bill of Materials

- KY-040 Rotary Encoder [5-pack, $9.29 (Amazon)](https://www.amazon.com/gp/product/B06XQTHDRR)
- Adafruit USB Micro-B Breakout Board [$5.60 (Amazon)](https://www.amazon.com/gp/product/B00KLDPZVU)
- Arduino Pro Micro [Clone, $12.60 (Amazon)](https://www.amazon.com/gp/product/B012FOV17O)
- 6 MX Mechanical Keycaps [e.g. Blank 24-pack XDA, $8.90 (Amazon)](https://www.amazon.com/gp/product/B095C47PJW)
- ~38mm Potentiometer Knob [$12 (Amazon)](https://www.amazon.com/gp/product/B087M2QCC2)
- 3D Printer + Filament
- 2x Micro USB 2.0 Cables
- 6x MX Mechanical Switches of your choice
- 26 AWG Solid Core Wire
- Soldering iron, Solder, Flux, Wire strippers, etc.

Estimated maximum cost: ~$50-$60

You can easily save money by 3D printing keycaps and the potentiometer knob, and by using any mechanical switches and USB cables you may have lying around.

## Instructions

*TODO*: step-by-step instructions

### 3D Printing

3D printing STLs are in the Case folder

*TODO*: 3D printing tips, settings, etc

### Wiring

[Wiring Diagram](Wiring/Macropad%20Wiring.jpeg)

*TODO*: Wiring instructions, photos

### QMK Firmware

Firmware is in the qmk/taylorpad folder.

The included default keymap uses volume controls for the rotary encoder, numpad key 0 for rotary switch, and numpad keys 1 through 6 for the switches.

The `encoder_num` keymap changes the rotary encoder to use the 7 and 8 keys, and is included in case you have trouble remapping volume keycodes (reported to have issues on MacOS)

The following instructions have only been tested on MacOS, and users on Windows or Linux systems may have to do a bit of tweaking along the way (mainly in the QMK toolbox section)

1. Follow the QMK "getting started" guide to install QMK - https://beta.docs.qmk.fm/tutorial/newbs_getting_started - steps 1 through 3.
2. Install QMK Toolbox

3. Symlink the qmk/taylorpad folder in this repository to the `~/qmk_firmware/keyboards/handwired` directory.
    - `git clone https://github.com/sbeck14/TaylorPad`
    - `ln -s [git_directory]/TaylorPad/qmk/taylorpad ~/qmk_firmware/keyboards/handwired`
4. Compile the firmware using the `qmk compile` command.
    - `qmk compile -kb handwired/taylorpad -km default`
    - This will place the `.hex` file in `~/qmk_firmware/.build/handwired_taylorpad_encoder_num.hex`
5. Get a flashing tool. This guide will use QMK Toolbox
    - Easiest (MacOS/Windows) - install QMK Toolbox https://github.com/qmk/qmk_toolbox/releases
    - If you are using Linux, you will have to use https://beta.docs.qmk.fm/tutorial/newbs_flashing#flash-your-keyboard-from-the-command-line instead. You'll be on your own from here on out (for now)
6. Open QMK Toolbox.
7. Put the Arduino into DFU mode
    - Bridge the GND and RST pins briefly with a bit of wire
    - The Arduino should immediately be recognized by QMK Toolbox
8. Open the hex file (`~/qmk_firmware/.build/handwired_taylorpad_encoder_num.hex`) with QMK Toolbox
9. Click Flash
10. Wait a few seconds, and you're done! Try it out!
