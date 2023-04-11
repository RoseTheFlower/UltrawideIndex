Although the solutions available here do not get tested on Linux before their release, Linux users have documented ways to get the solutions to work on their systems.

### Instructions for DLL-based solutions
#### Global
In Wine configuration, go to Libraries and add a new override for the applicable DLL libraries to be `native`, `builtin`.
#### Steam-specific
On Steam, add `WINEDLLOVERRIDES="dsound=n,b" %command%` as a launch option, where `dsound` is the name of the .dll file.
