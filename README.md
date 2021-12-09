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

The included keymap uses volume controls for the rotary encoder, numpad key 0 for rotary switch, and numpad keys 1 through 6 for the switches.

*TODO*: flashing instructions