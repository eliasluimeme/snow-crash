# Level09 - Writeup

Category : Cryptography / Reverse Engineering

Goal: reverse the custom token transformation.

Approach:
1. Test binary output with known inputs.
2. Observe rule: output[i] = input[i] + i.
3. Reverse rule for token bytes: plain[i] = cipher[i] - i.
4. Use decoded password for flag09 and run getflag.

Why this works:
- The cipher is deterministic and position-based, so inversion is direct.