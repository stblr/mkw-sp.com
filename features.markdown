---
layout: default
title: Features
permalink: /features/
---

## Features

**Custom Save System** [stebler]<br />
The rksys.dat format is replaced with a custom system that can support more than 4 licenses (for now the UI can [handle up to 6](/assets/6-licenses.png)) and [additional settings](/assets/license-settings.png). Ghosts are moved to separate files and everything is always unlocked. Riivolution's redirect feature is used to store all files to the SD card (or equivalent) instead of the NAND.

**11-Way Multi-Ghost** [stebler]<br />
It is possible to race against or watch up to [11 ghosts at once](/assets/11-ghosts.png). One can switch between ghosts during a replay (similar to live view). The ghost selection UI has been [accordingly remade from scratch](/assets/ghost-selection.png).

**Tag Limit Increase** [stebler]<br />
Up to 12 tags can be shown at once (from 3 in the vanilla game).

**Speedometer** [stebler]<br />
The speed of the player is shown in the HUD, including [moving road](/assets/som-moving-road.png) and [moving water](/assets/som-moving-water.png). Split-screen [is supported](/assets/som-split-screen.png).

**Additional Ghost Metadata** [stebler, Chadderz, MrBean35000vr, CLF78]<br />
The sha-1 of the track, whether 200cc was enabled, more precise finish times and detected glitches are saved at the end of the ghost file. The first two properties are used to only show ghosts for the correct track and engine class. The equivalent fields can be read from CTGP ghosts for the same purpose. The sha-1 computation doesn't take \_Dif files into account, allowing for e.g. custom textures.

**My Stuff Folder**<br />
Allows for file replacements such as custom tracks, custom music and so on. For tracks and UI files, it is possible to replace only certain U8 subfiles by adding the \_Dif suffix to the archive name (e.g. koopa\_course\_Dif.szs or MenuSingle\_E\_Dif.szs).

**Automatic BRSAR Patching** [Elias_]<br />
The revo\_kart.brsar file is automatically patched to prevent music from cutting off mid-race.

**Rear View In Replay** [stebler]<br />
In ghost replay mode, cinematic view is [replaced by rear view](/assets/rear-view.png).

**Hide HUD Labels** [stebler]<br />
_License setting._ The TIME, LAP and SPEED HUD labels are hidden.

**4:3 FOV in 16:9** [Brandondorf9999]<br />
_License setting._ The wider 4:3 field-of-view is used in 16:9 mode.

**Mii Heads On Minimap** [stebler]<br />
_License setting._ For local players and ghosts, the Mii replaces the character as minimap icon.

**200cc** [MrBean35000vr]<br />
_VS and time trial rule._ A speed class with a 1.5x speed multiplier, brake drifting and fast falling.

**Ghost Sorting** [stebler]<br />
_Time trial rule._ In the selection UI and in race ghosts can be sorted by finish time or by creation date.

**Ghost Tag Visibility** [stebler]<br />
_Time trial rule._ Ghost tags can be shown for all, focused only or no ghost.

**Ghost Tag Content** [stebler]<br />
_Time trial rule._ Ghost tags can be either the Mii name, [finish time](/assets/tag-time.png) or [creation date](/assets/tag-date.png).

**Solid Ghosts** [stebler]<br />
_Time trial rule._ Transparency can be disabled for all, focused only or no ghost.

## Limitations and known bugs

The name of ghost files can be at most 12 characters. This will not be fixed.

Ghost solidity is off by one frame when switching. See [issue 44](https://github.com/stblr/mkw-sp/issues/44).

VS and battle settings aren't saved. See [issue 50](https://github.com/stblr/mkw-sp/issues/50).

Most gecko codes won't work because of the different memory map. A warning is shown on the title screen if they are enabled. When memory protection is implemented, support will be dropped altogether.