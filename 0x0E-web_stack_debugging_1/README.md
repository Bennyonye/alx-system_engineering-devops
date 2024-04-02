# Web stack debugging #1

This project was part of a series focused on debugging web stacks. Each project involved identifying and fixing issues within isolated containers containing broken web stacks. For each task, I created scripts to automate the necessary commands to restore the web stack to a functional state.

## Tasks

* **0. Nginx likes port 80**
  * [0-nginx_likes_port_80](./0-nginx_likes_port_80): Bash script that configures Nginx to run and listen on port 80 for all active IPv4 addresses on the server.

* **1. Make it sweet and short**
  * [1-debugging_made_short](./1-debugging_made_short): Bash script that configures Nginx to listen on port 80 without binding to all active IPv4 addresses.
