# 0x05. Processes and signals
##### DevOps Shell Bash Syscall Scripting


## About Bash projects
Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.

## Resources
Read or watch:

1. Linux PID
2. Linux process
3. Linux signal
4. Process management in linux

man or help:

* ps
* pgrep
* pkill
* kill
* exit
* trap

## General Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

1. What is a PID
2. What is a process
3. How to find a process’ PID
4. How to kill a process
5. What is a signal
6. What are the 2 signals that cannot be ignored

## General Requirements

1. Allowed editors: vi, vim, emacs
2. All your files will be interpreted on Ubuntu 20.04 LTS
3. All your files should end with a new line
4. A README.md file, at the root of the folder of the project, is mandatory
5. All your Bash script files must be executable
6. Your Bash script must pass Shellcheck (version 0.7.0 via apt-get) without any error
7. The first line of all your Bash scripts should be exactly #!/usr/bin/env bash
8. The second line of all your Bash scripts should be a comment explaining what is the script doing

### More Info
For those who want to know more and learn about all signals, check out this article.(https://www.computerhope.com/unix/signals.htm)


Tasks

0. What is my PID: Writing a Bash script that displays its own PID.

1. List your processes: Writing a Bash script that displays a list of currently running processes.
It must require the below:
* it must show all processes, for all users, including those which might not have a TTY
* it should display in a user-oriented format
* it must show process hierarchy

2. Show your Bash PID: Writing a Bash script that displays lines containing the *bash* word, thus allowing you to easily get the PID of your Bash process.
NOTE:
* You cannot use pgrep
* The third line of your script must be __# shellcheck disable=SC2009__

3. Show your Bash PID made easy: Writing a Bash script that displays the PID, along with the process name, of processes whose name contain the word bash.
NOTE:
* You cannot use __ps__

4. To infinity and beyond: Writing a Bash script that displays To infinity and beyond indefinitely.
NOTE:
* In between each iteration of the loop, add a sleep 2

5. Don't stop me now!: Writing a Bash script that stops 4-to_infinity_and_beyond process.
NOTE:
* You must use kill

6. Stop me if you can: Writing a Bash script that stops 4-to_infinity_and_beyond process.
NOTE:
*You cannot use kill or killall

7. Highlander: Writing a Bash script that displays the below;
* To infinity and beyond indefinitely
* With a sleep 2 in between each iteration
* I am invincible!!! when receiving a SIGTERM signal

NOTE: Make a copy of your 6-stop_me_if_you_can script, name it 67-stop_me_if_you_can, that kills the 7-highlander process instead of the 4-to_infinity_and_beyond one.

8. Beheaded process: Writing a Bash script that kills the process 7-highlander.

9. Process and PID file: Writing a Bash script that does the below;
* Creates the file /var/run/myscript.pid containing its PID
* Displays To infinity and beyond indefinitely
* Displays I hate the kill command when receiving a SIGTERM signal
* Displays Y U no love me?! when receiving a SIGINT signal
* Deletes the file /var/run/myscript.pid and terminates itself when receiving a SIGQUIT or SIGTERM signal

10. Manage my process: 
* Writing a manage_my_process Bash script that indefinitely writes I am alive! to the file /tmp/my_process & also In between every I am alive! message, the program should pause for 2 seconds
* Writing Bash (init) script 101-manage_my_process that manages manage_my_process. (both files need to be pushed to git)

It must require the below:
1. When passing the argument start:
- Starts manage_my_process
- Creates a file containing its PID in /var/run/my_process.pid
- Displays manage_my_process started
2. When passing the argument stop:
- Stops manage_my_process
- Deletes the file /var/run/my_process.pid
- Displays manage_my_process stopped
3. When passing the argument restart
- Stops manage_my_process
- Deletes the file /var/run/my_process.pid
- Starts manage_my_process
- Creates a file containing its PID in /var/run/my_process.pid
- Displays manage_my_process restarted
4. Displays Usage: manage_my_process {start|stop|restart} if any other argument or no argument is passed

11. Zombie: Writing a C program that creates 5 zombie processes.
It must require the below:
* For every zombie process created, it displays Zombie process created, PID: ZOMBIE_PID
* Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
* When your code is done creating the parent process and the zombies, use the function bellow

## Copyright - Plagiarism
* You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
* You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
* You are not allowed to publish any content of this project.
* Any form of plagiarism is strictly forbidden and will result in removal from the program.

@BennyOnye
