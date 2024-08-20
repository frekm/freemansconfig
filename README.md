# Freeman's config

## Contents
- [Installation](#installation)
    - [Install config](#install-config)
    - [Unnstall config](#uninstall-config)
- [Included scripts](#included-scripts)
    - [Weaponslot-dependent settings](#weaponslot-dependent-settings)
    - [Custom "last weapon used" behaviour](#custom-last-weapon-used-behaviour)
    - [Movement script](#movement-script)
    - [Killing Floor-like voicemenu](#killing-floor-like-voicemenu)
    - [Class-specific scripts](#class-specific-scripts)
        - [Soldier and Pyro](#soldier-and-pyro)
        - [Demoman](#demoman)
        - [Engineer](#engineer)
        - [Medic](#medic)

## Installation 
### Install config:
- Go to the [Release page]() and download the latest release.
- Unpack the `.zip` file to
  `..\Steam\steamapps\*accountname*\common\Team Fortress 2\tf\custom`

- In case of new installation:
    + In `..\custom\freemansconfig\cfg\`, rename `settings_backup.cfg` to
      `settings.cfg` and edit your settings in this file
    + Rename `echos_backup.cfg` to `echos.cfg` and adjust the amount
      of "echos" according to your screen (this is the vertical padding
      of the onscreen menus)
    + Start TF2 and open keyboard settings
    + Press `Use defaults`, then edit the bindings to your likings

### Uninstall config
- Delete `..\custom\freemansconfig`
- Start Tf2 and open keyboard settings
- Press `Use defaults`, then edit the bindings to your likings

## Included scripts
### Weaponslot-dependent settings
Set up weaponslot-dependet settings in `settings.cfg`. More specialised
weaponslots will overwrite less specialised ones. The hierarchy is
- `slot<X>_<particular_class>` overwrites `all_slots_<particular_class>`
- `all_slots_<particular_class>` overwrites `slot<X>_all_classes`
- `slot<X>_all_classes` overwrites `all_slots_all_classes`
- If not overwritten, `all_slots_all_classes` applies to every weaponslot
  of every class

### Custom "last weapon used" behaviour
The default "last weapon used" behaviour (default Q) can switch between 
specific weaponslots instead of just switching to the last weapon used.

For example, when using `toggle_last_weapon_used_12X`, pressing Q switches:
- weaponslot1 always to slot2
- weaponslot2 always to slot1
- weaponslot3 to whatever was use before (i.e., slot1 or slot2)

This is controlled in `settings.cfg`. See there for all available options.

> **Note**<br>
> Each class has default and an alt settings. You can switch between them
> using the "Menu" key (default SHIFT).

### Movement script
Normally, moving forwards/left prevents the player from moving
backwards/right. The movement script allows doing that. It can be enabled
on a per-class basis in `settings.cfg`.

### Killing Floor-like voicemenu
If you know Killing Floor (1), you love its voicemenu. Added a voicemenu that
more or less ís the same.

To enable, bind it to a key in the keyboard settings.
Once you've opened the voicemenu ingame, you can close it/go one menu back
by hitting the voicemenu-key again.

### Class-specific scripts
#### Soldier and Pyro
"Rocketjump" performs jump, crouch, and attack at the same time. It can be
enabled/disabled per weaponslot for Soldier and Pyro in `settings.cfg` with
`rocketjump_script_enabled`/`rocketjump_script_disabled`.

#### Demoman
When using shields, a lazy person may want to always switch to melee weapons
when charging. This behaviour can be enabled/disabled with
`attack2_switches_to_melee`/`attack2_default` for Demoman.

This is disabled by default.

#### Engineer
Engineer has a build-script. Use it by pressing and holding ALT (by default).
Then
- Pressing 1: Cycle between building and destroying sentries (1x build, 2x 
  destroy, 3x build, ...)
- Pressing 2: Same for dispensers
- Pressing 3: Same for teleporter entries
- Pressing 4: Same for teleporter exits

#### Medic
If desired, one can always switch to the medicgun when hitting alt-attack
(thus, activating uber from "any" weaponslot). This is enabled/disabled
using `attack2_activates_ubercharge`/`attack2_default`.

This is enabled by default.