# Level03 - Simple Writeup

Category: Binary Exploitation / Privilege Escalation

Goal: exploit SUID binary command resolution.

Approach:
1. Run ltrace on level03.
2. Notice it calls /usr/bin/env echo.
3. Create a fake echo executable that runs getflag.
4. Put your writable directory first in PATH.
5. Execute level03.

Why this works:
- The SUID program resolves echo via PATH, so attacker-controlled echo runs first.