# Level01 - Writeup

Category: Password Hash Cracking

Goal: crack flag01 password hash.

Approach:
1. Read /etc/passwd and identify flag01 hash.
2. Recognize DES-crypt format (13 chars, no modern prefix).
3. Use a dictionary cracker.
4. Login as flag01 and run getflag.

Why this works:
- Legacy DES password hashes are weak against dictionary attacks.
