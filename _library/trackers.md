---
title: Trackers
author: {{site.author}}
last_modified_at: 2023-09-06
categories: [music]
---


Trackers were a popular way of composing music on a computer before traditional DAWs gained popularity.
They were often used for music in video games and by the [demoscene](https://en.wikipedia.org/wiki/Demoscene) and in the [jungle/drum and bass](https://www.youtube.com/watch?v=WV1McEtejxo) scene.
Their distinctive quality is a top down in time workflow (rather than the traditional left and right that is popular today) and heavy emphasis on samples.

## software

There are not many modern trackers around, [Renoise](https://www.renoise.com/) is the most popular modern tracker and has most of the features of any other DAW making it possible to create incredibly polished sounding tracks.
There is also [SunVox](https://warmplace.ru/soft/sunvox/) which is a hybrid of a tracker and modular synth environment.

There are also a few remakes of old software and open source options.

- [FastTracker II remake](https://16-bits.org/ft2.php)
- [ProTracker 2 remake](https://16-bits.org/pt2.php)
- [Milky Tracker](https://milkytracker.org/)
- [Schism Tracker](http://schismtracker.org/) ([Impulse tracker](http://www.users.on.net/~jtlim/ImpulseTracker/) clone)
- [openMPT](https://openmpt.org/) is a more modern open source tracker.
- [BambooTracker](https://bambootracker.github.io/BambooTracker/) is a modern 4 op FM tracker to help you make music for old consoles.

## hardware

In recent years an interest in a hardware form of the tracker workflow has emerged with projects like the game boy [lsdj](https://www.littlesounddj.com/lsd/index.php).
[lpgt](https://www.littlegptracker.com/) is inspired by lsdj but is available on much more hardware as well as traditional PCs.
In eurorack format there is the [NerdSeq](https://xor-electronics.com/nerdseq/) and in standalone hardware there is the [Polyend Tracker](https://polyend.com/tracker/) and the [Dirtywave M8](https://dirtywave.com/).

the [tic80](https://link) fantasy console also has a [music editor](https://github.com/nesbox/TIC-80/wiki/Music-editor) with a tracker workflow and can be used to make chiptunes

## example music

- [Polyend tracker](https://www.youtube.com/watch?v=P7xlaPDzF84)
- [nerdseq](https://www.youtube.com/watch?v=9TquD64S8v0)
- [renoise](https://www.youtube.com/watch?v=TNJzCaybzOk)
- [(mitch murder renoise fun)](https://www.youtube.com/watch?v=GSJKQ2B9R3Q)
- old [pro tracker music](https://www.youtube.com/watch?v=cJJsWN8Afaw)
- more old [pro tracker music](https://www.youtube.com/watch?v=Z2dQxRy9df4)
- [John Frusciante breakcore](https://www.youtube.com/watch?v=3qBDrdZVCpQ)
- [Polyend tracker glitch hop](https://www.youtube.com/watch?v=TIT94QVBjJY)

## making music with trackers

### tic 80

in order for your music to play you need the following code saved to your *.tic.

```lua
music_started=false
function TIC()
    if not music_started then
        music(0)
        music_started=true
    end
end
```

### hardware specific tools

if you intend on making music for different systems like NES, SNES, SEGA Genesis, etc. then there are plenty of tools you can use:

- [SNES Tracker](https://github.com/bazz1tv/snestracker/wiki)

## getting into the tracker/chip scene

- botb
- irc (esper.net)
  - \#modulez
  - \#mod_shrine
  - \#botb
- compos
  - [all sorts of battles](https://battleofthebits.org/)
  - [one hour comps](http://wiki.s3m.us/)
    - [uploader for hosting a comp](https://s3m.it/stats)

## chiptune adjacent communities

[weekly beats](https://weeklybeats.com/) is run by the creator of the m8 tracker and is a year long challenge to create one track a week (only run on even years).
