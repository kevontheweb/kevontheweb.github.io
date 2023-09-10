---
title: "UXN On ESP32 For A Hardware Orca Sequencer"
last_modified_at: 2023-01-06
---

**NOTE: I HAVE NOT MADE FURTHER PROGRESS ON THIS AS OF WRITING. PLEASE CHECK OUT [MAX22's UXN ESP32 PORT](https://github.com/max22-/uxn-esp32)**

*edit: It may also be simpler to port orca-c directly and not attempt to port the entire UXN virtual computer.*

## inspiration

I have recently been quite inspired by old tracker software and the few [hardware trackers](/knowledge/music/trackers.md) that are out now.

After hanging around on [merveilles](https://merveilles.town) i discovered [orca](https://github.com/hundredrabbits/Orca-c) and the [uxn virtual computer](https://100r.co/site/uxn.html) (both by [hundred rabbits](https://github.com/hundredrabbits)) and thought that it might be possible to run orca as a rom on an esp32 using uxn.
Especially since the esp32 is such a capable microcontroller [(even IBM PC DOS has been emulated on it!)](https://hackaday.com/2021/07/28/emulating-the-ibm-pc-on-an-esp32/)

Orca is an esoteric programming language used to sequence midi devices and is often used in [livecoding (video example)](https://www.youtube.com/watch?v=4VSrjp0w3jA) [(wikipedia)](https://en.wikipedia.org/wiki/Live_coding).

It is possible to build any style sequencer you can imagine even including things like randomness and [euclidean rhythms (video explanation)](https://www.youtube.com/watch?v=OHS3lN6snrE) [(wikipedia)](https://en.wikipedia.org/wiki/Euclidean_rhythm).
[Tracker style sequencers have also been made with Orca](https://www.youtube.com/watch?v=nKAjx6n97IY)

## resources

luckily there was already a well documented [uxn tutorial](https://compudanzas.et/uxn_tutorial.html).
The screen and mouse has already been implemented but audio and keyboard are still in progress.

## hardware

I already had an esp32cam dev board with an sd card slot and a 128*64 i2c oled, but not all the pins are made available on this dev board and this screen is too small for most uses in uxn and is also only black and white.

### processing

an esp32 dev board will be used as the main processor

### output

A better alternative would be to use an ILI9341 based (or similiar) SPI TFT LCD
since SPI TFT displays are supported through the use of the [TFT_eSPI library](https://github.com/Bodmer/TFT_eSPI)

### input

For user input USB keyboard/MIDI could be added with a MAX3421

## software

[eps32 uxn port](https://github.com/max22-/uxn-esp32) is a port of [uxnemu](https://git.sr.ht/~rabbits/uxn/tree/master/item/src/uxnemu.c) to the esp32 platform.

UXN uses [sdl](https://wiki.libsdl.org/) and [portmidi](http://portmedia.sourceforge.net/portmidi/) to provide a cross platform interface (on computers) and midi device usage.

Unfortunately sdl and portmidi are not available for esp32 so something else will have to take it's place:

some other libraries that can be used to take the place of sdl and port midi:

- [This arduino library](https://github.com/felis/USB_Host_Shield_2.0) for the [MAX3421](https://datasheets.maximintegrated.com/en/ds/MAX3421E.pdf) could add usb peripheral support over SPI (including MIDI and HID).

## design

### controls

#### Option 1

Inspired by the LARGE multifunction encoder (knob) on the polyend tracker I thought it might be useful to use a rotary encoder with push button.
It moves left/right when not pressed down and up and down when the encoder is pressed.

a few common keys like

- arrow cluster
- ctrl
- shift
- backspace

as well as a numpad with layers so that all 36 keys needed can be pressed without the need for a full size keyboard (though the ability to plug in a full size keyboard in the future would be nice.)

#### Option 2

Use a PS2 keyboard or serial

### interface

The visual user interface on the LCD will be provided by the UXN roms

## usage

The idea would be to be able to use it to sequence midi devices or use as part of a modular synth (if used in conjunction with a midi to cv device)

## todo

- [ ] try make the oled work then get an lcd if necessary
- [ ] my esp32 has psram so it should be fine?
- [ ] figure out something for keyboard inputs

## last resort (just use a pi)

- [diy norns](https://llllllll.co/t/diy-norns-shield/27638)
- [diy teletype](https://llllllll.co/t/teletype-diy-using-grid-keyboard-at-the-same-time-no-switch/39716)
