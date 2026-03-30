# Level10 steps
nc -lk 6969
# in another shell:
gcc resources/time_of_check_time_of_use.c -o /tmp/level10_race -lpthread
/tmp/level10_race