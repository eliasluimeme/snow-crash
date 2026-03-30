# Level03 steps
ltrace ./level03
mkdir -p /tmp/level03 && cd /tmp/level03
cp /Users/elias/git/snowcrash/snowcrash/level03/resources/main.c .
gcc main.c -o echo
chmod +x echo
export PATH=/tmp/level03:$PATH
/home/user/level03/level03
