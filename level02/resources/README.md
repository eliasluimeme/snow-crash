# Level02 - Writeup

Category : Network Forensics / Traffic Analysis

Goal: recover credentials from a network capture.

Approach:
1. Locate level02.pcap.
2. Open it in Wireshark or tshark.
3. Follow TCP stream and inspect data in ASCII plus hex.
4. Reconstruct typed password and handle backspaces.
5. Login as flag02 and run getflag.

Why this works:
- Credentials were sent in cleartext in the captured session.
