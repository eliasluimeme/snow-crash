# Level08 - Simple Writeup

Goal: bypass filename check to read protected token.

Simple approach:
1. Run ltrace and find strstr(path, "token") check.
2. Create a symlink with a safe name pointing to token.
3. Execute binary with symlink path.

Why this works:
- Program validates the input string, not the final resolved file.