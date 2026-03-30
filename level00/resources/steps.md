# Level00 steps
find / -user flag00 2>/dev/null
# Option A (Python helper):
python3 resources/Caesar_decypher.py
# Option B (C++ helper):
g++ resources/decode.cpp -o /tmp/decode00 && /tmp/decode00
# expected decode -> nottoohardhere
su flag00
getflag
