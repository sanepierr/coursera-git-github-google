This reading explains how to apply changes to files using diff and patch. Instead of manually editing files after someone suggests fixes, developers can generate a diff file that shows exactly what changed and then automatically apply those changes using the patch command.


The script checks CPU usage using the psutil module and prints a warning if usage exceeds 75 percent.

A colleague discovers that the script always reports that everything is fine, even when the system is overloaded.
```#!/usr/bin/env python3

import psutil

def check_cpu_usage(percent):
    usage = psutil.cpu_percent()
    return usage < percent

if not check_cpu_usage(75):
    print("ERROR! CPU is overloaded")
else:
    print("Everything ok")
```
The Diff File

Instead of sending the entire modified script, the colleague sends a diff file that contains only the changes.

```
--- cpu_usage.py
+++ cpu_usage_fixed.py
@@ -2,7 +2,8 @@
 import psutil

 def check_cpu_usage(percent):
-    usage = psutil.cpu_percent()
+    usage = psutil.cpu_percent(1)
+    print("DEBUG: usage: {}".format(usage))
     return usage < percent

```

Two changes were made:

The function cpu_percent() now includes a parameter to average usage over one second.

A debug print statement was added to display the CPU usage value.

**Applying the Patch**

Instead of manually editing the file, the patch command can apply the changes automatically.

```
patch cpu_usage.py < cpu_usage.diff
```
After running this command, the file is updated with the changes from the diff.

**Updated Script After Patching**

```
#!/usr/bin/env python3

import psutil

def check_cpu_usage(percent):
    usage = psutil.cpu_percent(1)
    print("DEBUG: usage: {}".format(usage))
    return usage < percent

if not check_cpu_usage(75):
    print("ERROR! CPU is overloaded")
else:
    print("Everything ok")

```

**Why Use Diff and Patch Instead of Sending the Whole File?**

There are several advantages:

Only the actual changes are shared, making them easier to review.

The patch can still apply even if the original file has minor differences.

It preserves project structure when modifying multiple files.

It clearly shows what was changed and why.

**Key Takeaway**

The diff command is used to generate a file that captures changes between versions of a file or directory. The patch command applies those changes automatically. Together, these tools help developers share, review, and apply updates efficiently, forming the foundation of modern version control systems like Git.