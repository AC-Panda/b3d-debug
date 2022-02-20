# How to debug a Blender 3D rash

## Prerequisites

You'll need the `blender_debug_log.cmd` script found in this Github repository.

Double-check to see if your root Blender folder doesn't already have it to avoid an unnecessary download.

**Note:** In recent UPBGE 0.2.x releases UPBGE was not shipped with CMD script and will need to be downloaded manually.

## Instructions

1. Run the (`blender_debug_log.cmd`) CMD script by clicking it from your root Blender folder
2. A `terminal window` should open once the script is clicked: `hover` your `mouse-cursor` over the generated terminal window
3. Once the `terminal window` is `active`, push the `ENTER` key to confirm opening of Blender, and Blender should open normally
4. Attempt to make Blender crash again; and when it does, `File Explorer` should automatically open a new Explorer window that contains a newly generated folder containting the crash logs
5. In the generated crash logs folder, make sure to view `blender_debug_output.txt` and NOT `blender_system_info.txt` to prevent wasting time

**SPECIAL MENTIONS:** Please understand that Blender may **NOT** crash while running it from the debug terminal, as some exception alerts have been disabled

# Additional info for debugging exported BGE projects
7. Most likely after exporting a blend file as an executable, it's going to have a file-name other than 'Blender'
So in the `blender_debug_log.cmd` script, rename the line:
```
"%~dp0\blender"
```
To
```
"%~dp0\PROJECT_NAME"
```
To allow the CMD script to regonize the desired runtime.
