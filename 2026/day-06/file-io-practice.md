

ubuntu@ip-172-31-25-52:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-25-52:~$ touch notes.txt -- created an empty file with touch file_name command
ubuntu@ip-172-31-25-52:~$ echo "these are the notes for Linux" > notes.txt -- > operator is used to insert a text in a file
ubuntu@ip-172-31-25-52:~$ echo "these can be used for DevOps troubleshooting" > notes.txt
ubuntu@ip-172-31-25-52:~$ echo "make sure do the hands on these commands" > notes.txt
ubuntu@ip-172-31-25-52:~$ cat notes.txt -- cat is used to view the content from a file. 
                                            Now i have added 3 lines but only 1st line was taken because > it takes only first line.
make sure do the hands on these commands
ubuntu@ip-172-31-25-52:~$ 

ubuntu@ip-172-31-25-52:~$ cat notes.txt
make sure do the hands on these commands
ubuntu@ip-172-31-25-52:~$ echo "hello" >> notes.txt -- >> operator will append the file and it will not override the existing text.
ubuntu@ip-172-31-25-52:~$ cat notes.txt 
make sure do the hands on these commands
hello
ubuntu@ip-172-31-25-52:~$ echo "do more practice on Linux" >> notes.txt
ubuntu@ip-172-31-25-52:~$ cat notes.txt
make sure do the hands on these commands
hello
do more practice on Linux
ubuntu@ip-172-31-25-52:~$ 

ubuntu@ip-172-31-25-52:~$ echo "now line4 was adeed here " | tee -a notes.txt -- this will add a new line in real time and give output what is added newly.
now line4 was adeed here 
ubuntu@ip-172-31-25-52:~$ cat notes.txt 
make sure do the hands on these commands
hello
do more practice on Linux
now line4 was adeed here 
ubuntu@ip-172-31-25-52:~$ 
