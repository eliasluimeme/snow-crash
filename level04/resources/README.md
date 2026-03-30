# Level04 - Writeup

Category: Web Application Security / Command Injection

Goal: inject command into CGI parameter.

Approach:
1. Read level04.pl and find unsanitized backtick execution.
2. Send payload through HTTP query parameter x.
3. Execute getflag in injected command context.

Why this works:
- User input is concatenated into shell command and executed with elevated rights.
