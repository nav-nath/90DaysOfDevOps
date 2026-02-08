For today's session, done the hands on below commands.

1> Logs into AWS ubuntu instance
2> uname - check the username who logged in
3> pwd - to check the present working directory
4> mkdir - created a 2-3 new directories
5> cd - change directory
6> touch - to create an empty file
7> top - to view the summary of memory, processes, PID etc -- screen shot attached.


Able to install nginx server on EC2 install
(To install anything on Linux require root permission hence used sudo)

sudo apt update -- This will update the apps on system

sudo apt install nginx -y -- This will install nginx server on EC2 instance. -y gives Yes whenever asked.

to check the status of nginx/any other installed aplication

systemctl status nginx -- It will give the status of nginx which is active (not running)

to make it run, have to run with below commands

sudo systemctl start nginx
