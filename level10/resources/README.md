# Level10 - Simple Writeup

Goal: exploit TOCTOU race between access() and open().

Simple approach:
1. Run ltrace and confirm access() check then open().
2. Start a listener on port 6969.
3. Race a writable file path with symlink swaps to token.
4. Capture leaked token on listener.

Why this works:
- access() uses real uid while open() happens later with effective uid in SUID flow.