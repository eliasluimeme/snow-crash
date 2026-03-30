# Level07 - Writeup

Category : Binary Exploitation / Environment Variable Injection

Goal: inject via environment variable.

Approach:
1. Trace binary and observe getenv("LOGNAME") plus system(...).
2. Set LOGNAME to command payload.
3. Execute binary and capture getflag output.

Why this works:
- Untrusted environment variable is embedded in shell command in SUID context.