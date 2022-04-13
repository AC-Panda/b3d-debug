## How to debug a Blender3D (or BGE/UPBGE) when it crashes

### Prerequisites

* `blender_debug_log.cmd`
* Windows OS (feel free to convert the script for your operating-system)

Blender 2.8+ usually ships with it, so no need to download it if you already have the script locally. You can double-check if you have it by searching in your root `Blender` folder. If your Blender/UPBGE folder doesn't have this script, you can download it from this Github repository.

### Instructions

1. Place `blender_debug_log.cmd` in your root Blender if it already isn't there.
2. Run the (`blender_debug_log.cmd`) CMD script by clicking it.
3. A `terminal` window should open, once so `hover` your `mouse-cursor` over the generated terminal window.
4. Once the `terminal` window is `active` or `in focus`, push the `ENTER` key to confirm opening of Blender and Blender should open normally.
5. Attempt to make Blender crash again; and when it does, `File Explorer` should automatically open a new Explorer window containing a new `TEMP` folder containting the generated crash logs.
6. In the new crash logs folder, make sure to view `blender_debug_output.txt` and not `blender_system_info.txt` to prevent wasting time your time.
<br>**NOTE:** Please be aware that Blender may **NOT** crash while running the debug terminal is open, as some exception alerts have been disabled.

## How to debug a exported BGE/UPBGE runtime

0. If your exported runtime has a file name other than `Blender` or `blender` e.g.:

```
Game.exe
```

You'll need to tweak the CMD script to recognize your runtime in order to launch and debug it.

1. Edit your `blender_debug_log.cmd` CMD script and rename the line:

```
"%~dp0\blender"
```

to

```
"%~dp0\%PROJECT_NAME%"
```

`%PROJECT_NAME%` should be the file name of your exported runtime such as `Game`.<br />No need to add your executable's extension type (exe, app, elf, etc).
