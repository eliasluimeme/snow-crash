# Level10 - Writeup

Category: Privilege Escalation / SUID Exploit

Goal: exploit TOCTOU race between access() and open().

Approach:
1. Run ltrace and confirm access() check then open().
2. Start a listener on port 6969.
3. Use provided helper source `toctou.c` to race a writable file path with symlink swaps to token.
4. Capture leaked token on listener.

Why this works:
- access() uses real uid while open() happens later with effective uid in SUID flow.

Resource used:
- `toctou.c`