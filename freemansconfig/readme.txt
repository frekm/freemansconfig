*** Freeman's Config - simple v1.2.0 ***

*** Contents ******************************************************************
1. Installation
2. Generell scripts
    2.1. Weaponslot dependent settings
    2.2. Custom quickswitch behaviour
    2.3. Movement script
    2.4. Killing Floor-like voicemenu
    2.5. Spawnswap script
3. Class specific scripts
    3.1. Soldier
    3.2. Pyro
    3.3. Demoman
    3.4. Medic
    3.5. Engineer
4. Update notes


*** Installation **************************************************************
1.1. Install config:
    - Unpack to
      '..\Steam\steamapps\*accountname*\common\team fortress 2\tf\custom'

    - In case of new installation:
        + In '..\custom\freemansconfig\cfg\', rename '_settings_backup.cfg' to
          '_settings.cfg' and edit your settings in this file
        + Start TF2 and open keyboard settings
        + Press 'Use defaults', then edit the bindings to your likings

1.2. Uninstall config
    - Delete ..\custom\freemansconfig\
    - Start Tf2 and open keyboard settings
    - Press 'Use defaults', then edit the bindings to your likings


*** Generell scripts **********************************************************
2.1. Weaponslot dependent settings
    Set up weaponslot dependet settings in '_settings.cfg'. More specialised
    weaponslots will overwrite less specialised ones; e.g. 'slot1_cls' will 
    overwrite the settings in 'slots_all', 'slot1_scout' will overwrite
    settings in 'slot1_cls' etc.

2.2. Custom quickswitch behaviour
    Quickswitch (default Q) can switch between specific weaponslots instead of
    just switching to the last used weapon. These settings can be changed
    on-the-fly ingame with a pop-up-menu (default SHIFT). Default quickswitch
    behaviour is specified in '_settings.cfg'.

2.3. Movement script
    Normally, moving forwards/left prevents the player from moving
    backwards/right. The movement script allows doing that.

2.4. Killing Floor-like voicemenu
    If you know Killing Floor, you love its voicemenu. Added a voicemenu that
    more or less ís the same.
    To enable, bind it to a key in the keyboard settings.
    Once you've opened the voicemenu ingame, you can close it/go one menu back
    by hitting the voicemenu-key again.

2.5. Spawnswap scripts
    Quickly switch to another class, then switch back to your old class by
    hitting the spawnswap-key again. Only works if you don't spam it too
    quickly (before you actually joined as another class). If you spam it too
    quickly, it breaks and you will not spawn as your desired class. You then
    manually have to switch to your class again (or reload config, there's a
    keybind option for it in the keyboard-settings).

2.6. Ingame menu
    Change your quickswitch behaviour and enable some class specific scripts
    on the fly.


*** Class specific scripts ****************************************************
3.1. Soldier
    - Rocketjump-script: Performs Crouchjump-attack with one buttonpress, won't
        give you the best rocketjumps, but does the trick if you're lazy

3.2. Pyro
    - Panicbutton: Spin around like crazy while screaming in agony and burning
        them all.

3.3. Demoman
    - Different behaviour depending on which weapon you choose as your
      secondary (you have to choose your loadout in the ingame-menu, the script
      cannot detect which weapon you actually have equipped. Choose the default
      setting in '_settings.cfg'):
        Stickies: usual behaviour
        Shields:  Always quickswitch between melee and primary; switch to melee
                  and charge when alt-attacking.

3.4. Medic
    - alt-attack always switches to medicgun and charges if your ubercharge is
      ready.

3.5. Engineer
    - Buildscript:
        Classkey + 1x 1-4: build a sentry/dispenser/tele-entrance/tele-exit
        Classkey + 2x 1-4: destroy respective building


*** Update notes **************************************************************
v1.2.0
    Removed unnecessary files in .rar-file
    Removed disguise-weaponswitcher-script to keep things simple
    Removed temporary viewmodel toggle because I never used it
    Removed temporary xhair-toggle because why
    Added possibility to choose jump-type per class
    Updated readme.txt
    Updated config_default.cfg

v1.1.8
    Fixed some bugs with the voicemenu

v1.1.7
    Added Killing Floor-like voicemenu.

v1.1.6
    Updated for Steampipe

v1.1.5
    Added Disguise-Weapon-Changer Script for spy
    Added support for mousewheel-usage

v1.1.4
    Added 'Reload Config' command

v1.1.3
    Updated 'kb_act.lst' and 'config_default.cfg'

v1.1.2
    Updated 'kb_act.lst' and 'config_default.cfg'

v1.1.1
    Fixed menu not working properly for demoman
    Fixed spawnswap script

v1.1.0
    Reworked config, because Valve fucked up the "con_logfile" command
         - saving ON-THE-FLY is no longer possible
         - simplified menus
         - removed record-script
         - to change settings:
             - hold the "menu"-key and press 1-5 to change settings
             - settings will no longer be saved permanantly, restarting game or
               changing class will reset settings to default.
             - changed _settings.cfg

v1.0.1
    Removed necessity of autoexec.cfg
    Fixed movementscript
    Added readme.txt

v1.0.0
    Release

