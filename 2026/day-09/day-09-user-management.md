-- Today learings on User Management

-- Creating a new user with home directory access
   sudo useradd -m tokio
cd /home
ubuntu@ip-172-31-25-52:/home$ ls -lrt
total 8
drwxr-x--- 7 ubuntu ubuntu 4096 Feb 13 01:52 ubuntu
drwxr-x--- 2 tokyo  tokio  4096 Feb 13 02:10 tokio

ubuntu@ip-172-31-25-52:/home$ sudo useradd -m Berlin
ubuntu@ip-172-31-25-52:/home$ sudo useradd -m Professor
ubuntu@ip-172-31-25-52:/home$ ls -lrt
total 16
drwxr-x--- 7 ubuntu    ubuntu    4096 Feb 13 01:52 ubuntu
drwxr-x--- 2 tokyo     tokio     4096 Feb 13 02:10 tokio
drwxr-x--- 2 Berlin    Berlin    4096 Feb 13 02:18 Berlin
drwxr-x--- 2 Professor Professor 4096 Feb 13 02:18 Professor

Now cat /etc/passwd file to view the password related info.

ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash
tokyo:x:1001:1001::/home/tokio:/bin/sh
Berlin:x:1002:1002::/home/Berlin:/bin/sh
Professor:x:1003:1003::/home/Professor:/bin/sh

created 2 groups as below

ubuntu@ip-172-31-25-52:/$ pwd
/
ubuntu@ip-172-31-25-52:/$ sudo groupadd admin
groupadd: group 'admin' already exists
ubuntu@ip-172-31-25-52:/$ sudo groupadd developers
ubuntu@ip-172-31-25-52:/$ sudo groupadd admins

-- Adding users to groups
sudo usermod -aG group_name user_name -a → append (important! prevents removing user from other groups), G - group name.
ubuntu@ip-172-31-25-52:/$ sudo usermod -aG admins Professor
ubuntu@ip-172-31-25-52:/$ sudo usermod -aG developers tokyo
ubuntu@ip-172-31-25-52:/$ sudo usermod -aG admins Berlin
ubuntu@ip-172-31-25-52:/$ sudo usermod -aG developers Berlin
