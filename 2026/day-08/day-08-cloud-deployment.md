Launched an EC2 instance.
Installed ngnix with below command
    sudo apt update -- This will update the apps on system
    sudo apt install nginx -y -- This will install nginx server on EC2 instance. -y gives Yes whenever asked.
systemctl status nginx -- to check the status of nginx
sudo systemctl start nginx -- to start the nginx server.

Copid the public ip of an istance and tried to open it. It didn't worked because security group was not allowing http trafic.

--> Instance -> Security Group -> Edit Inboud Rules - IP Range -> Anywhere (Port 80 by default)

Then hit the publi Ip again and got the webpage http://http://34.209.54.33
