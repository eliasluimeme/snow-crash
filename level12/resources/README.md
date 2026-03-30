# Level12 - Simple Writeup

Goal: bypass CGI input filtering and still execute command.

Simple approach:
1. Review Perl CGI logic and input transformations.
2. Place attacker script in /tmp with executable permission.
3. Trigger script execution through crafted request using command substitution path.
4. Read output file written by script.

Why this works:
- Filtering is incomplete and shell expansion still permits attacker-controlled execution.