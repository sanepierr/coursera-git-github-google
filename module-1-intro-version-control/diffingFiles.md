This reading introduces the diff tool, which is used to compare different versions of files and clearly show what has changed between them. It demonstrates how diff works line by line to highlight removed, added, or modified lines, making it easier to track changes in code over time.

**Comparing simple file changes**

Two versions of a Python script are compared. The main change is an update to the regular expression so it supports hyphens in names.


```diff rearrange1.py rearrange2.py```

```6c6
<     result = re.search(r"^([\w .]*), ([\w .]*)$", name)
---
>     result = re.search(r"^([\w .-]*), ([\w .-]*)$", name)
```

This output shows exactly which line was changed and how the newer version differs from the older one.

**Comparing files with multiple changes**

When files become more complex, diff can show several changes at once. In the example below, input validation logic is modified and new checks are added.

```diff validations1.py validations2.py```

```
5c5,6
<	assert (type(username) == str), "username must be a string"
--
>	if type(username) != str:
>	    raise TypeError("username must be a string")

11a13,15
>	# Usernames can't begin with a number
>	if username[0].isnumeric():
>	    return False

```
This output makes it clear which lines were replaced and which new logic was introduced.

**Using unified diff format**

The reading also introduces the unified diff format, which is commonly used in version control systems because it provides more context around each change.

```diff -u validations1.py validations2.py```

```--- validations1.py
+++ validations2.py
@@ -2,7 +2,8 @@
-    assert type(username) == str, "username must be a string"
+    if type(username) != str:
+        raise TypeError("username must be a string")

@@ -10,5 +11,8 @@
+    # Usernames can't begin with a number
+    if username[0].isnumeric():
+        return False
```

The unified format shows surrounding lines, which helps explain how each change fits into the overall file.

**Key takeaway**

The diff tool makes it easy to understand how files change over time by clearly showing what was added, removed, or modified. This is a core concept behind version control systems like Git, where being able to review and understand changes is essential for collaboration, debugging, and maintaining clean code.