Although the solutions available here do not get tested on Linux before their release, Linux users have documented ways to get the solutions to work on their systems.

### General suggestions
When using a solution that needs to target the running game process, [ensure](https://github.com/RoseTheFlower/UltrawideIndex/issues/25#issuecomment-1650838775) that both run within the same Wine prefix. Consider trying [Bottles](https://usebottles.com/), which may simplify the process.

### Instructions for DLL-based solutions
The instructions below apply to the solutions that require dropping a DLL file into the game folder.
#### Global
In Wine configuration, go to Libraries and add a new override for the applicable DLL libraries to be `native`, `builtin`.
#### Steam-specific
On Steam, add `WINEDLLOVERRIDES="dsound=n,b" %command%` as a launch option, where `dsound` is the name of the .dll file.
