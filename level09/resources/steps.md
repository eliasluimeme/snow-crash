# Level09 steps
./level09 a
./level09 ab
./level09 abc
# infer shift-by-index behavior and reverse token content
cat token | hd
# Option A (C helper):
gcc resources/decode.c -o /tmp/decode09 && /tmp/decode09
# Option B (Python helper):
python3 resources/hex_shift.py
# then:
su flag09
getflag