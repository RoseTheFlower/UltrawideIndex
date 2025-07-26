Although the solutions available here do not get tested on Linux before their release, Linux users have documented ways to get the solutions to work on their systems.

# General suggestions
When using a solution that needs to target the running game process, [ensure](https://github.com/RoseTheFlower/UltrawideIndex/issues/25#issuecomment-1650838775) that both run within the same Wine prefix. Consider trying [Bottles](https://usebottles.com/), which may simplify the process.

### Instructions for DLL-based solutions
The instructions below apply to the solutions that require dropping a DLL file into the game folder.
#### Global
In Wine configuration, go to Libraries and add a new override for the applicable DLL libraries to be `native`, `builtin`.
#### Steam-specific
On Steam, add `WINEDLLOVERRIDES="dsound=n,b" %command%` as a launch option, where `dsound` is the name of the .dll file.

# SteamTinkerLaunch Guide
### Install STL
- [Install Guide](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Installation)
- In Steam select your Game and select SteamTinkerLaunch as the compatibility tool

### Install UltrawideIndex
- Follow the Instruction specific to your game

### Configure STL to start the Ultrawide Fix
- Start the Game and select Main Menu (or press space) once the STL Popup shows up
- Select Category --> Misc
- Select "Use Custom command
- In the Custom Command Field use the file Chooser and select the Ultrawide.exe
- Select "Fork custom command"
- Deselect "Use Steam Linux Runtime with Custom Command"
- Select "Inject custom command
- set "Inject wait" depending on game 15 seconds is probably fine
- Press "Save and Play"

The game should now start and after the selected wait the Fix should get injected

