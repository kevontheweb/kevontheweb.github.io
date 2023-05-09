---
title: Satellites
---

You can use the [heavens above site](https://heavens-above.com/AmateurSats.aspx) or [n2yo](https://www.n2yo.com/) to see what satellites are passing you and when.

Here is a collection of the satellite that I have decoded transmissions from.

## NOAA Weather Satellites

The NOAAx satellites are weather satellites that broadcast a satellite image over VHF using the [APT (Autmatic Picture Transmission) protocol](https://en.wikipedia.org/wiki/Automatic_picture_transmission)
They were commisioned by the [National Oceanic and Atmospheric Administration](https://www.noaa.gov/weather)

The two that often orbit over me are the [NOAA-15](https://en.wikipedia.org/wiki/NOAA-15) and the [NOAA-19](https://en.wikipedia.org/wiki/NOAA-19).

### Finding out when its passing

for that you can use the [heavens above site](https://heavens-above.com/AmateurSats.aspx) or the [Look4Sat android app](https://github.com/rt-bishop/Look4Sat).

![example view for the NOAA 19 satellite on heavens-above.com](/assets/images/other/heavens-above.png)

The start and end times are when the satellite is passing and the altitude and azimuth are the angle and direction respectively.
a 90&deg; azimuth is directly over your head.
you can use this information to help you orient yourself when you try to record the signal.

### recording the signal

I used my baofeng uv5r to listen in on the frequency specified in the Look4Sat android app (137.62MHz in my case)

I recorded the audio using my cellphone. (I recorded a video but audio only would probably work better)

The longer and clearer recording you can get the better the final image will be.

I then stripped the audio from the video using ffmpeg

```ffmpeg -i video.mp4 -c:v copy -vn audio.wav```

### using wxtoimg

If you are on windows you can use wxtoimg to decode your audio into a satellite image

wxtoimg is abandonware and getting hold of a copy can be a bit tricky with all the reposted copies available.
I used [this link](https://www.wraase.de/wxtoimg/) to get my installer.

The software is old enough that the windows version should work without issues in wine on linux but there is [better software](https://noaa-apt.mbernardi.com.ar/download.html) available on linux.

The audio then needs to be mixed down to mono and resampled at 11025Hz to match the requirements for wxtoimg

the audio then needs to be saved as a .wav file.

This can be done using Audacity

> note: if you have ffmpeg installed audacity may be able to automatically extract the audio from a video file on import

![GIF showing the processing of the audio preparing it for wxtoimg in audacity](/assets/images/other/noaa15-audacity.gif)

the audio can then be imported into wxtoimg and it will be automatically processed into an image

### using noaa-apt

[get noaa-apt here](https://noaa-apt.mbernardi.com.ar/download.html)

### results

My first attempt went quite poorly

![My first attempt at getting a sattelite image from one of the NOAA weather sattelites using my Baofeng uv5r](/assets/images/other/noaa-first-attempt.png)

On my second attempt i was able to see some border informaiton and part of an image on the left

![My second attempt at getting a sattelite image from one of the NOAA weather sattelites using my Baofeng uv5r](/assets/images/other/noaa-second-attempt.png)

but after giving it few more shots and taking a much longer recording I was able to decode a pretty decent image.

![The best result I got from the baofeng (false color)](/assets/images/other/noaa-19-boafeng-best-false-color.png)

![The best result I got from the baofeng (raw+IR)](/assets/images/other/noaa-19-boafeng-best.png)

Here is a false color image and the raw+infrared image (you can make out some clouds as well as the west side of Africa)

The [boafeng](/gear/ham.md#baofeng-uv5r-uhfvhf-radio) doesn't really have enough bandwidth to get a full quality image and it's really easy to accidentally move and mess up the signal (which you can see in the vertical lines)

I still haven't managed to get my SDR working for this.
(I think i might need a different antenna) but it should provide much better image quality.

### tips

1. try to get as long a recording as possible without too many interferences.
2. recording the direct audio out from the headphone out into some kind of audio interface may provide cleaner recordings
3. using a better [antenna](radio.md#antennae) could also help

I will be trying this again with an antenna and an SDR which should provide higher bandwidth (and thus more data) for a better quality image.

### references

[RTL-SDR blog - Antennae for NOAA](https://www.rtl-sdr.com/rtl-sdr-tutorial-receiving-noaa-weather-satellite-images/)

[Modern Ham - Decoding NOAA Weather Satellites with BaoFeng Radio](https://youtu.be/LUDOzCM0SRI)

[Tech Minds - Decoding Weather Satellites Using An SDR Receiver NOAA-19](https://youtu.be/4wXjsCvHKI0)

## GOES 16 and 17 weather sats

[rtl-sdr blog - GOES 16/17 and GK-2A Weather Satellite Reception Comprehensive Tutorial](https://www.rtl-sdr.com/rtl-sdr-com-goes-16-17-and-gk-2a-weather-satellite-reception-comprehensive-tutorial/)

## iss

you have to check the [ariss  website](https://www.ariss.org/) to see when the iss will be transmitting

sometimes they broadcast an image over [sstv](radio.md#sstv)

[How to get pictures from the International Space Station via amateur radio](https://www.youtube.com/watch?v=HtC-BPcMruA)
