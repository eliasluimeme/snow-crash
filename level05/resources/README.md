# Level05 - Writeup

Category: Privilege Escalation / Cron Job Exploitation

Goal: abuse scheduled script execution.

Approach:
1. Check mail and cron hints.
2. Find a script that periodically executes files from a writable location.
3. Drop a tiny script that runs getflag and writes output to /tmp.
4. Wait for cron tick and read output.

Why this works:
- A privileged cron task executes attacker-controlled script files.