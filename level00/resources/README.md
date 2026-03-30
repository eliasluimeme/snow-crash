# Level00 - Writeup

Category: Password / Cipher Cracking

Goal: recover the password hidden in files owned by flag00.

Approach:
1. Search files owned by flag00.
2. Find a suspicious lowercase string.
3. Try Caesar/ROT shifts until plaintext appears.
4. Use the decoded password to switch user and run getflag.

Why this works:
- The stored string is a basic Caesar cipher, not a real hash.
