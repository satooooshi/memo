test

lab3:ref:https://github.com/TongRuizheWithGzz/CSE-labs/tree/lab3

sudo docker run -it --privileged --cap-add=ALL -v /Users/satoshiaikawa/cse2019/lab-cse/lab1:/home/stu/devlop ddnirvana/cselab_env:latest /bin/bash

su root
password: 000

make clean

export RPC_LOSSY=5
./lock_server 3772 &
./lock_client
kill -9 [pid]
ps ux | grep [prog_name]

