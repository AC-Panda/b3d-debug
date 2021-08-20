# Steps To Debug Blender 3D

Use blender_debug_log.cmd which can be found in your main Blender folder to debug Blender crashes.

- Run the cmd script, then click the **`enter`** key while hovering over the activated cmd window
- Blender should be run then, and when it crashes, your computer's file explorer should open a window containing a newly created folder with the debug prints
- Make sure to look at **`blender_debug_output.txt`**, not **`blender_system_info.txt`** to prevent wasting time
The output file contains the crash logs while the other file contains other information that is unrelated to crashes
