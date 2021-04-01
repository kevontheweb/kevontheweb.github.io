---
title: "Better Zen Mode for VSCode"
author: Kevin Nel
last_modified_at: 2020-04-22
categories: [tech]
---

If you, like me, moved over to VSCode after using sublime you probably miss the very uncluttered interface and simple  design, but can't give up all the great features and extensions of Visual Studio Code.

Well as with most problems regarding VSCode *There's an extension for that*.

![zen](/assets/images/zenmode.gif)

## Step 1

So step 1 is to download the [vscode settings cycler](https://marketplace.visualstudio.com/items?itemName=hoovercj.vscode-settings-cycler) extension which will allow you to cycle between sets of settings in VSCode.

## Step 2

Step 2 is to add the following lines to your ``settings.json``.

If you dont know how to open your ``settings.json`` you can open it by pressing ``ctrl+shift+p`` and then typing ``settings`` this bring up the option to either open your settings.json or open settings UI. select the settings.json and hit enter.

![VSCode Settings](/assets/images/settingsjson.gif)

```json
"settings.cycle": [
        {
            "id": "sublimeMode", // must be unique
            "overrideWorkspaceSettings": true,
            "values": [
                {
                    "editor.minimap.enabled": true,
                    "workbench.statusBar.visible": true,
                    "editor.renderIndentGuides": true,
                    "workbench.activityBar.visible": true,
                    "workbench.editor.showTabs": true,
                    "breadcrumbs.enabled": true,
                    "editor.wordWrapColumn": 120,
                },
                {
                    "editor.minimap.enabled": false,
                    "workbench.statusBar.visible": false,
                    "editor.renderIndentGuides": false,
                    "workbench.activityBar.visible": false,
                    "workbench.iconTheme": null,
                    "workbench.editor.showTabs": false,
                    "breadcrumbs.enabled": false,
                    "editor.wordWrapColumn": 80,
                }
            ]
        }
    ],
```

If you want to customize anything you can just add the setting as you would into your ``settings.json`` and its corresponding alternative into the above.

## Step 3

in order to assign a keyboard shortcut to these sets of settings you have to add the following to your ``keybindings.json``.

You can open the ``keybindings.json`` file the same way as for ``settings.json``. Just search for ``keyboard shortcut``

![VSCode Keybindings](/assets/images/keybindingsjson.gif)

```json
{
"key": "shift+f11",
"command": "settings.cycle.sublimeMode",
}
```

## Step 4

You're done!
