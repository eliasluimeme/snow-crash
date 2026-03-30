# Level13 - Simple Writeup

Goal: bypass UID check (expects UID 4242).

Simplest practical approach:
1. Reverse quickly (ltrace/strings) to confirm getuid() check against 4242.
2. In a controlled lab machine, create a user with UID 4242.
3. Run the binary as that user.

Why this works:
- Program gates success on UID value only; matching UID satisfies branch condition.