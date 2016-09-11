# PoGoMap-GUI

## Description
This is a GUI tool created to ease the process of running your pokemongo-map and creating new accounts to scan with. This combines a few tools created by other users on github. This is a windows only tool. Sorry for my horrible coding but so far it seems to get the job done!

Tools being used by my GUI:
 - Pokemongo-Map (https://github.com/PokemonGoMap/PokemonGo-Map)
 - Pikaptcha (https://github.com/sriyegna/Pikaptcha)
 - PokeAlarm (https://github.com/kvangent/PokeAlarm)
 - PoGoAccountCheck (https://github.com/a-moss/PoGoAccountCheck)
 - Pokemongo-Map IVs and movesets (https://github.com/MangoScango/PokemonGo-Map/tree/IVs-and-Moves)

## Features
![Alt text](https://github.com/engle2192/PoGoMap-GUI/blob/master/Screenshots/MainGUI.PNG)
 - Run your map in spiral scan or spawn point scanning
 - Enable/Disable scan for poke stops, gyms, fixed locations, no search control
 - Choose step limit (step limit must be commented out in your PokemonGo-Map config.ini for this to work)
 - Set starting location (location must be commented out in your PokemonGo-Map config.ini for this to work)
 - Quickly create accounts and automatically add them to your PokemonGo-Map config.ini (Please check the wiki for instructions https://github.com/engle2192/PoGoMap-GUI/wiki)
 - Quickly check the accounts you are currently using and automatically delete banned or deleted accounts from your config.ini
 - Command windows now dock in the GUI
 - 2Captcha Key, Password, and Location field will save through application restarts

## Installation
3. Download latest PoGoMap-GUI zip from releases section. (https://github.com/engle2192/PoGoMap-GUI/releases)
4. Extract files to a folder.
7. Follow the bellow instructions to configure your computer to bypass execution policy for powershell scripts
8. Run PokemonGo-Map_Launcher.exe
9. Click the "Download PreReqs" at the bottom. Follow steps 1-3 on the new window that opens.
10. After those steps are complete you should now be able to run your map! Dont forget to add a starting zip code location! To view your map open a browser and go to http://YOUR_IP:5000

## Powershell instructions
1. Run below in powershell launched as administrator:

    Set-ItemProperty -Path HKLM:\Software\Policies\Microsoft\Windows\PowerShell -Name ExecutionPolicy -Value ByPass

2. If you get this error continue to step 3 other wise you are finished.
![Alt text](https://i0.wp.com/absolute-sharepoint.com/wp-content/uploads/2014/03/031714_2013_ChangethePo5.png?w=940)
3. This is because your local group policy to allow scripts to run on the system is probably “not configured” . To configure it, run “gpedit.msc”
4. Then Navigate to: Computer Configuration > Administrative Templates > Windows Components > Windows PowerShell. Change the “Turn on Script Execution” to look something like this:![Alt text](https://i2.wp.com/absolute-sharepoint.com/wp-content/uploads/2014/03/031714_2013_ChangethePo7.png?w=940)
5. Afterwards, the PowerShell command should work and you should be able to change your Execution Policy without any problems!
![Alt text](https://i2.wp.com/absolute-sharepoint.com/wp-content/uploads/2014/03/031714_2013_ChangethePo8.png?w=940)
