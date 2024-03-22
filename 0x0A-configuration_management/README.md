# Puppet Configuration Management

This project introduces the use of Puppet as a configuration management tool. Puppet manifests are utilized to perform various tasks such as creating files, installing packages, and executing commands.

## Task Summaries

* **0. Creating a File**
  * [0-create_a_file.pp](./0-create_a_file.pp): Defines a Puppet manifest to create a file named `school` in the `/tmp` directory with specific permissions, group, owner, and content.

* **1. Installing a Package**
  * [1-install_a_package.pp](./1-install_a_package.pp): Implements a Puppet manifest to install the `flask` package using `pip3`.

* **2. Executing a Command**
  * [2-execute_a_command.pp](./2-execute_a_command.pp): Utilizes a Puppet manifest to terminate the process named `killmenow`.

These manifests serve to automate system configuration tasks, enhancing efficiency and reliability in managing infrastructure.
