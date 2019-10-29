
# https://ipads.se.sjtu.edu.cn/courses/cse/labs/Lab1.html

# superheatedboy

# Commands

sudo docker run -it --privileged --cap-add=ALL -v /Users/satoshiaikawa/cse2019/lab-cse/lab1:/home/stu/devlop ddnirvana/cselab_env:latest /bin/bash

vscode diff 
compare 

# memo
- cf1: copied all from https://github.com/satooooshi/cse/blob/master/lab1finished/inode_manager.cc

- su root
password: 000
then 
sudo ./start.sh
~


git pull は remote先に存在するlocal branch名 を　checkoutしてから!! lab1dev で git pull してもremoteに存在しないからkaraできないよ!!


lab2 yfs_client not found

su root
sudo make clean
sudo make
sudo ./grade.sh

git stash
git checkout other_branch

AFTER you have implement all features above, run the grading script:

part 1
su root
cd devlop/lab1
make rpcdemo
./demo_server 3772 &
./demo_client 3772
then you can see
stat request from clt 332171483
stat returned 0

part 2a
su root
cd devlop/lab1
make
./lock_server 3772 &
 ./lock_demo 3772
 then you can see
 stat request from clt 1349653701
stat returned 0

You must register handlers for these RPCs with the RPC server object (register acquire & release inside lock_smain.cc).

./lock_server 3772 &
./lock_tester 3772
then you see
 ./lock_tester: passed all tests successfully


# To avoid annoying git-merge issues  
mkdir newdir; cd newdir; (enter a clean directory)
% git clone https://ipads.se.sjtu.edu.cn:1312/lab/cse-2019-fall.git;
% cd cse-2019-fall; git checkout lab3;
% cp rpc/librpc64.a PATH_TO_MY_LAB_DIR/rpc/;

# resolve the conflicts (by editing the relevant files) and then run 'git commit -a'): --amend, 可以覆蓋當前分支最前面的提交 
