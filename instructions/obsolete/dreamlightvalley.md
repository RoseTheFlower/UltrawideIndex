For Steam users, there is a way to launch Dreamlight Valley and [the solution](/../../releases/tag/dreamlightvalley) via a single file.

1. Download and extract the archive of the fix.
2. Right-click and Edit **RunFix.bat** to add the following lines after the first line:
```bat
start steam://rungameid/1401590
timeout /t 20 /nobreak
```
3. Save the file and use it.

This will launch the game, then wait 20 seconds before automatically applying the fix. The value is fully adjustable.

Credits to Angered Fox for the suggestion.
