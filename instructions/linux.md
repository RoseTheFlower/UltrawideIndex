Although the solutions available here do not get tested on Linux before their release, Linux users have documented ways to get the solutions to work on their systems.

## General suggestions
When using a solution that needs to target the running game process, [ensure](https://github.com/RoseTheFlower/UltrawideIndex/issues/25#issuecomment-1650838775) that both run within the same Wine prefix. Consider trying [Bottles](https://usebottles.com/), which may simplify the process.

## Instructions for DLL-based solutions
The instructions below apply to the solutions that require dropping a DLL file into the game folder.
### Global
In Wine configuration, go to Libraries and add a new override for the applicable DLL libraries to be `native`, `builtin`.
### Steam-specific
On Steam, add `WINEDLLOVERRIDES="dsound=n,b" %command%` as a launch option, where `dsound` is the name of the .dll file.

## Instructions for standalone injection-based solutions
The instructions below apply to the solutions that require running an app after the game in order to target its process (e.g a trainer).
### Steam-specific
#### Steam Tinker Launch
*(based on Squiddim's guide submitted to this repository)*
1. [Install Steam Tinker Launch](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Installation).
1. Download the desired trainer-based solution found in this repository.
1. In the Steam client, go to the game's properties and set *Steam Tinker Launch* as the compatibility tool.
1. Launch the game from Steam and select Main Menu (or press Space) once the Steam Tinker Launch window shows up.
1. In the Steam Tinker Launch window, select Category -> Misc.
1. Select *Use Custom Command*.
1. In the Custom Command field, use the file chooser and select the trainer exe.
1. Select *Fork custom command*.
1. Deselect *Use Steam Linux Runtime with Custom Command*.
1. Select *Inject custom command*.
1. Set *Inject wait* depending on the game (15 seconds are probably a good value).
1. Press *Save and Play*.
