---
title: "Windows VSTs On Linux"
author: {{site.author}}
last_modified_at: 2021-07-16
categories: [music,tech]
---

I am in the process of setting up a [linux](/knowledge/linux.md) workstation for music production and one of the challenges has been migrating my **MASSIVE** collection of windows plugins to linux.

Fortunately a lot of my favorite plugins already have linux versions, but for the plugins that don't I need to install them in wine and run them with a vst bridge

## using ``yabridge``

yabridge is a vst bridge for running windows vsts in linux DAWs.
Unlike Carla yabridge has no GUI so the plugins load into your DAW just like you would expect and you don't have to use a work around to run your plugins.

There is decent tutorial on the [yabridge github repo](https://github.com/robbert-vdh/yabridge#usage), but here's the short version:

1. install ``yabridge`` and ``yabridge-ctl`` (and make sure it is in your ``$PATH``)
2. install your windows vst in [wine](https://www.winehq.org/) by runnning ``wine Some_Random_VST_plugin_win64.exe`` and then run through the installer (you can leave all paths default).
3. after the windows vst has been successfully installed in wine run ``yabridgectl list`` to see which plugin directories have already have been added to yabridge.
4. run ``yabridgectl add ".wine/c_drive/Your Plugin Directory"`` to add any directories that you have installed plugins to that are not already in yabridge.
5. run ``yabridgectl sync`` to let yabridge setup all the plugins.
6. every time you install some windows vsts in wine, repeat step 5 to sync your plugins.

> Be sure to check the [yabridge github repo](https://github.com/robbert-vdh/yabridge#usage) for more help.
I have tested a few drm fre plugins in [Reaper](/knowledge/music/reaper.md) as well as the windows version of [Vital](https://vital.audio) and most of the plugins ran fairly well.

## Other considerations for a linux music production workstation

yabridge is an amazing tool and makes running windows vsts on linux a breeze, but if the plugin you wish to use has a linux native version available, then use that first.
Native plugins will run much better than the same plugin running in wine with a bridge

Another thing to take note of is the packaging format that native linux vsts and plugins are provided as.
From my explorations into linux music production I have noticed that most of the native linux vsts are distributed as ``.deb`` package downloads and are often not available through a package manager.
This means that choosing a debian based distributions will provide the smoothest experience with the most software support
