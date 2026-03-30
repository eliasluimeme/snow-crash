# Level06 - Simple Writeup

Goal: exploit unsafe PHP preg_replace with /e.

Simple approach:
1. Inspect level06.php used by the binary.
2. Find preg_replace with the /e modifier.
3. Craft input matching [x ...] and inject command substitution.
4. Run level06 with crafted file.

Why this works:
- /e evaluates replacement as PHP code, enabling command execution.