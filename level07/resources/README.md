# Level07 - Simple Writeup

Goal: inject via environment variable.

Simple approach:
1. Trace binary and observe getenv("LOGNAME") plus system(...).
2. Set LOGNAME to command payload.
3. Execute binary and capture getflag output.

Why this works:
- Untrusted environment variable is embedded in shell command in SUID context.