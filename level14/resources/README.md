# Level14 - Simple Writeup

Category: Binary Exploitation / Anti-Debugging Bypass

Goal: pass final checks in getflag and retrieve final token.

Documented path:
1. Analyze getflag behavior with strings and static analysis.
2. Identify anti-debug checks (ptrace and preload checks) plus UID-based token selection.
3. In controlled environment, execute as UID matching flag14 (3014).

Why this works:
- Token output branch is selected by UID after integrity checks.