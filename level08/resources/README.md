# Level08 - Writeup

Category: Binary Exploitation / File Access Restriction

Goal: bypass filename check to read protected token.

Approach:
1. Run ltrace and find strstr(path, "token") check.
2. Create a symlink with a safe name pointing to token.
3. Execute binary with symlink path.

Why this works:
- Program validates the input string, not the final resolved file.