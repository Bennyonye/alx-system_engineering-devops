# Web Stack Debugging #3

This is the fourth project in a series focused on web stack debugging. In these projects, I worked with broken or bugged web stacks within isolated containers. My task was to identify and fix the issues, ensuring the web stack returned to a fully functional state. For each task, I created a script to automate the necessary commands for resolving the issues.

## Tasks :page_with_curl:

* **0. Strace is Your Friend**
  * [0-strace_is_your_friend.pp](./0-strace_is_your_friend.pp): A Puppet manifest designed to correct a typo that was causing a WordPress application, served by an Apache web server, to fail.
  * To use: `puppet apply 0-strace_is_your_friend.pp`
