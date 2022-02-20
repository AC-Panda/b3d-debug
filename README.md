# Steps To debug Blender 3D

Official Blender releases ship with the `blender_debug_log.cmd` script and can be found in the root directory of your Blender folder.

Note: In recent UPBGE 0.2.x releases UPBGE doesn't always ship with it so you may need to download the CMD script from this repository and manually place it inside your Blender's root folder.

Once you're sure that you have the CMD script, complete these following steps to get crash logs:
1. Run the CMD script (`blender_debug_log.cmd`) by clicking it while it's placed in your root Blender folder
2. Hover your mouse-cursor over the generated terminal window
3. Once the terminal window is active, push the `ENTER` key to confirm opening of Blender, and Blender should open normally
4. Attempt to make Blender crash again; and when it does, `File Explorer` should automatically open a new Explorer window that contains a newly generated folder containting the crash logs
5. Note_1: In the generated crash logs folder, view `blender_debug_output.txt` and not `blender_system_info.txt` to prevent wasting time
6. Note_2: Please understand that Blender may **NOT** crash while running it from the debug terminal, as some exception alerts have been disabled

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
