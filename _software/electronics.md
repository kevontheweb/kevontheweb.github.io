---
title: Electronics
author: {{site.author}}
last_modified_at: 2023-07-16
categories: [tech]
---
<!--
This is where I try to store all the information that I frequently forget or need a refresher on.

## connectors

crimp connectors often have a lip that can be pressed in order to remove the wires from the connector.

some common connectors are:

- jst
- dupont
- molex

[This video](https://www.youtube.com/watch?v=GZOh1NzqzzU) is a very thorough explanation of how to crimp many types of connectors.

-->
## Bugs That I Want To Document Because It Wasted A Lot Of My Time

### Unable To Communicate Over Serial With Hardware (Arduino, Ch341 Serial Etc) On Linux

1. Make sure you are in the ``uucp`` group.

  ```bash
  usermod -aG uucp $USER
  ```

2. Check if you have ``orca`` installed. ``brltty``, a dependency of orca, conflicts with the udev rules that assign ``/dev/ttyUSB*`` and other serial devices) uninstall ``orca`` and ``brltty`` and check if your problem is resolved.

  > You may need to log out and log back in for these fixes (definitely for number 1)

3. check dmesg output to see what is happening. (it may help if you still don't come right)

  ```bash
  dmesg -k | grep "ftdi"
  dmesg -k | grep "ttyUSB"
  dmesg -k | grep "ch34"
  ```

[source](https://www.ftdichip.com/Support/Documents/TechnicalNotes/TN_102_Customising_FTDI_VID_PID_In_Linux(FT_000081).pdf) that helped me figure it out

### intel quartus prime jtag, hardware not showing

The following script I wrote will help to reset the quartus jtag daemon

This quirk can be found documented [here](https://ecen3350.rocks/static/usb-blaster.pdf) and the [arch wiki page](https://wiki.archlinux.org/title/Intel_Quartus_Prime#Error_when_scanning_hardware_-_Server_error) was also helpful

```bash
#!/bin/bash

DIR=$(pwd)
cd ~/intelFPGA_lite/20.1/quartus/bin/;
sudo killall -9 jtagd;
sleep 2;
sudo ./jtagd;
sleep 3;
./jtagconfig;
cd $DIR;
```

## digital electronics

### bitwise operations

Multiplication by 2 can be accomplished by shifting the bits in a register to the left by 1

Division by 2 can be accomplished by shifting the bits in a register to the right by 1

Modulo as well as many other operations can be done similarly

See [this post](https://mastodon.social/@elbosso/106767096728015399) and [this article](https://graphics.stanford.edu/~seander/bithacks.html)

This [wiki on bitmath](https://bisqwit.iki.fi/story/howto/bitmath/) is also really good

## Software Tools

- [wokwi arduino simulator](https://wokwi.com/)
- [flux - collaborative EDA](https://www.flux.ai/p)
