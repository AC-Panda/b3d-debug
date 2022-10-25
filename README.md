# Guide to debugging Blender/BGE/UPBGE crashes 

### Prerequisites

* `blender_debug_log.cmd`
* Windows OS (feel free to convert the script for your OS)

**NOTE:** Blender 2.8+ versions usually ships with the script, so no need to download it if you already have the script locally. You can double-check if you have it already by searching in your root _Blender_ folder. If your Blender/UPBGE folder doesn't have this script, you can download it from this repository.

### How to generate crashlogs - Blender/BGE/UPBGE

1. Place `blender_debug_log.cmd` in your root Blender (if it isn't already there).
2. Run `blender_debug_log.cmd` by clicking it.
3. A _terminal_ window should open - once so, hover your _cursor_ over the generated terminal window.
4. Once the _terminal_ window is active or in focus, push the _ENTER_ key to confirm the opening of Blender - Blender should open normally then.
5. Attempt to make Blender crash again; when it does, _File Explorer_ should automatically open a new _Explorer_ window containing a new _TEMP_ folder, which should contain the newly generated crashlogs.
6. In the crashlogs folder, make sure to view `blender_debug_output.txt` and not `blender_system_info.txt` to prevent wasting time.

**NOTE:** Please be aware that Blender may _NOT_ crash while the debug terminal is still open, as most exception alerts have been automatically disabled.

## How to generate crashlogs - Exported Runtime

1. If your exported runtime has a filename other than _Blender_ or _blender_, for example `Game.exe`, you'll need to tweak the script to recognize your runtime in order for the script to properly launch and debug your runtime.

2. To edit the script to fit your renamed runtime, open your script in a text editor and rename: `"%~dp0\blender"` to `"%~dp0\%PROJECT_NAME%"`.

**NOTE:** `%PROJECT_NAME%` should be the filename of your runtime such as `Game`. No need to add your runtime's extension type (exe, app, elf, etc.), that's automatically detected.
