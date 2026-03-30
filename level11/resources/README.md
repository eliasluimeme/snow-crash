# Level11 - Simple Writeup

Goal: exploit Lua service command injection.

Simple approach:
1. Inspect level11.lua and find io.popen("echo "..pass.." | sha1sum").
2. Connect to local service with netcat.
3. Inject shell metacharacters in password field to run getflag.

Why this works:
- Untrusted input is concatenated into a shell command and executed.