---
title: amateur radio
---

I am currently in the process of acquiring my amateur radio licence but I have still had a chance to play around a bit.
On of my biggest interests is software defined radio which can be super powerful and makes it very easy (and cheap) to visualise the RF spectrum over really wide bandwidths.

## Why amateur radio is cool

Here is a collection of cool stuff that you can do with amateur radio.

This [excellent talk by Gerard de Jong](https://youtu.be/DREv1zpkVwM) goes over a lot of cool stuff you can do with sdr and amateur radio.

Here are some of my favorites (not all of these are from the above video):

- receive signals from [satellites](projects/satellites).
  - sstv on the iss
  - images on the NOAA weather sattelites (using wxtoimg)
- "hack" gate motors and other keyfob systems
  - older systems use simple dit dah  or on off transmissions
  - newer systems use [rolling codes](https://spencerwhyte.blogspot.com/2014/03/delay-attack-jam-intercept-and-replay.html)
  - [this talk about car keyfob hacks](https://www.youtube.com/watch?v=UNgvShN4USU)
- [receive images from computer monitors over radiated RF](https://www.rtl-sdr.com/tempestsdr-a-sdr-tool-for-eavesdropping-on-computer-screens-via-unintentionally-radiated-rf/)
  - [video demo](https://www.youtube.com/watch?v=mBJ6uQZsF9c)
- visualise air traffic using [ads-b](https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance%E2%80%93Broadcast)
- visualise ship traffic

You can also use a [raspberry pi](/knowledge/raspberrypi.md) to transmit radio signals.
Here are a few projects that allow you to do that.

- [rpitx](https://github.com/F5OEO/rpitx)
  - [rpitx tech minds](https://www.youtube.com/watch?v=Wsy-TAFNs90)
  - [rpitx sdr-blog](https://www.youtube.com/watch?v=ewY-woG1dNw)
- [pifmrds](https://github.com/ChristopheJacquet/PiFmRds)

## Resources

Some websites with good resources:

- [dxzone](https://www.dxzone.com/)
- [rtl-sdr](https://www.rtl-sdr.com/)

Some great content on youtube (mainly sdr stuff):

- [thought emporium's radio videos](https://youtube.com/playlist?list=PLZLsjPxmF1BEi7vH6Qo9lHMLW0WKdjDEV)
- [Tech Minds](https://www.youtube.com/channel/UC9a8Z6Sp6eb2s3O79pX5Zvg)
- [Hacking the Wireless World with Software Defined Radio - 2.0](https://www.youtube.com/watch?v=N0p3_ES2dBU)

## SDR

### rtl-sdr

The rtl-sdr comes from a digital TV chip that was "hacked" to receive a much wider range of signals than originally intended and now we have really cheap (receive only) sdrs

The rtl-sdr dongles can do hf with some work arounds, but are most comfortable in the range of 500 kHz - 1766 MHz, Depending on what [sdr software](#sdr-software) you use it can sample up to 24MHz but is most stable at 2.4MHz:

- [hf on rtl sdr using direct sampling](http://www.radioforeveryone.com/p/the-new-smart-manufacturer-link-can-do.html)
- [hf on rtl sdr using up converter](https://www.rtl-sdr.com/tag/upconverter/)

the rtl-sdr-blog radio has [a great datasheet](https://www.rtl-sdr.com/wp-content/uploads/2018/02/RTL-SDR-Blog-V3-Datasheet.pdf)

### SDR software

Here are some SDR softwares.
Personally, I User SDR++ and GQRX.

- [SigDigger](https://batchdrake.github.io/SigDigger/)
- [CubicSDR](https://github.com/cjcliffe/CubicSDR)
- [SDR++](https://github.com/AlexandreRouma/SDRPlusPlus)
- [GQRX](https://gqrx.dk/)
- [sdr-radio](https://www.sdr-radio.com/download) *windows only
- [sdr sharp]() *windows only

### GNU-Radio

I have not dedicated the time to learn gnu-radio but it seems like an extremely powerful toolkit for processing of RF signal (and signals in general).

- [michael ossmans gnu radio dsp sdr course](https://greatscottgadgets.com/sdr/)
- [using gnu radio with rtl sdr](https://www.rtl-sdr.com/tag/gnu-radio/)

## GPS

[meshtastic.org](https://meshtastic.org/) is a very cool concept for an open source off-grid mesh network, powered by LoRa-WAN, that uses relatively inexpensive microcontrollers.

## VHF/UHF

I have a [baofeng uv5-r](/gear/ham.md) for VHF/UHF

A lot of [satellites](satellites.md) and even the ISS use VHF/UHF

### Security Companies

In south africa a lot of radios targeted at security companies use the 464 and 446MHz UHF bands at 0.5 watts to avoid the need for a licence.

<!-- ![an example of a radio with some no-licence bands pre programmed in](/assets/images/other/zartek-no-licence-freq.png)
 -->

## Modes

you can use the [sigid wiki](https://www.sigidwiki.com/wiki/Database) to help identify a signal and aid in decoding it.

### SSTV

SSTV stands for slow scan television.

[SSTV on Wikipedia](https://en.wikipedia.org/wiki/Slow-scan_television)

[The ISS](satellites.md#ISS) sometimes transmits an image over sstv that you can receive and decode.

### FT-8

[what is ft8?](https://www.onallbands.com/ft8-what-is-it-and-how-can-i-get-started/)

### APRS

APRS stands for automatic packet reporting system.

see [APRS on Wikipedia](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System).

[Curious Electron article](https://www.curiouselectron.com/?p=595)

#### aprs on the [Baofeng uv5-r](/gear/ham.md)

In order to use aprs on the baofeng you need the appropriate cable and some software

The cable: BTECH APRS-K1 Cable

The software: aprs droid

Aprs required a [TNC (Terminal Node Controller)](https://en.wikipedia.org/wiki/Terminal_node_controller) in order to decode the signals.

TNC and AX.25 resources

- [arduino nano diy tnc](http://www.mobilinkd.com/2014/09/11/arduino-kiss-tnc/)
- [Dire Wolf - software "soundcard" AX.25 packet modem/TNC and APRS encoder/decoder](https://github.com/wb2osz/direwolf)
- [linux ax.25 packet radio setup](https://www.qbjnet.com/packet.html)

The aprs droid app is able to process the audio and decode aprs packets.

I have yet to try this out in real life as I do not have the appropriate cable.
There are some resources on making your own cable:

- [tnc-x cable](https://www.tnc-x.com/Baofeng.htm)
- [aprsdroid baofeng cable](https://willbradley.name/2015/08/09/aprs-via-rf-cable-for-connecting-aprsdroid-to-a-baofeng-radio/)
- [qsl.net](https://www.qsl.net/w6dps/APRSDroid.html)
- [pcb adapter](https://github.com/johnboiles/BaofengUV5R-TRRS)

Here is also a really cool [mobile aprs digital repeater](https://github.com/Rom3oDelta7/APRS-Mobile-Digipeater) built into a pelican case.

## antennae

to make any of these antennae you can just search "$ANTENNANAME calculator".
there are many different calculators that can assist in working out the measurements for the antennae.

### Yagi-Uda

The Yagi-Uda antenna has a bit of a thomas edison/nikola tesla telephone thing going on, it seems that Uda was largely responsible for it's creation but He worked under Yagi and thus the Yagi-Uda antenna was born.
It is most commonly just referred to as a Yagi.

![[Yagi-Uda on Wikipedia](https://en.wikipedia.org/wiki/Yagi%E2%80%93Uda_antenna)](/assets/images/other/Yagi-Uda.png)

The only decent calculator I could find was the [changpuak yagi-uda calculator based on the Rothammel / DL6WU design](https://www.changpuak.ch/electronics/yagi_uda_antenna_DL6WU.php) as well as the [changpuak yagi-uda calculator based on a constant spacing of 0.2 &lambda;](https://www.changpuak.ch/electronics/yagi_uda_antenna.php)

It seems that the yagi-uda antenna is fairly complex and requires a good bit of fine tuning and adjustment with iterative analysis.

The designs available online are therefore a lot more like "recipes" and there can be differences between 2 yagi-uda designs for the same frequency.
Here is [some history about the DL6WU design](https://www.qsl.net/vk2kfj/DL6WU.html).

### Cross Dipole

4 dipole antennae angled at 30&deg; arranged in a square across from each other.

A cross dipole is omnidirectional.

[qsl: designing a cross dipole for vhf and noaa sattelite receiving](https://www.qsl.net/py4zbz/DCA.pdf)

### Planar Disk

[planar disk antenna build guide pdf](https://www.wa5vjb.com/references/PlanarDiskAntennas.pdf)

### Turnstile

[turnstile antenna design for 137MHz](https://web.archive.org/web/20130827200955/http://www.digitalham.co.uk/weather/equipment/turnstile-antenna/)

![[Turnstile antenna on Wikipedia](https://en.wikipedia.org/wiki/Turnstile_antenna)](/assets/images/other/turnstile-antenna.png)

### V Dipole

[V Dipole for 137MHz NOAA sattelites](https://lna4all.blogspot.com/2017/02/diy-137-mhz-wx-sat-v-dipole-antenna.html)

### QFH

QFH stands for quadrifilar helicoidal antenna

[online calculator](https://www.jcoppens.com/ant/qfh/calc.en.php)
[3d printable bracket for 137MHz on thingiverse](https://www.thingiverse.com/thing:765794)

## Components

### connectors

- bnc
- sma
  - rp sma : has a pin in the male connector
  - sma : has a pin in the female connector
- mmcx/mxc

### cable

different types of coax are rated for different losses at different frequencies.

you can use online calculators ([like this old one](https://www.net-comber.com/cable-loss.html) or [this one by times microwave systems](https://www.timesmicrowave.com/calculator)) to see what you need for your frequency and length.

[different kinds of coax for different purposes](https://www.jpole-antenna.com/2013/01/12/what-type-of-feedline-coax-should-i-use-for-my-antenna/)
