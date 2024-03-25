# Web Server Configuration

This project delves into the fundamentals of web servers, covering their functionality and configuration. Using a personal server provided by ALX, I gained hands-on experience with `scp` and Fabric for file transfer and completed basic Nginx configuration.

The server is accessible at [bdbnb.site](http://bdbnb.site).

## Task Overview

* **0. File Transfer to Server**
  * [0-transfer_file](./0-transfer_file): Bash script for transferring a file from the local machine to the server using `scp`.
  * Arguments include file path, server IP, username, and SSH private key path.
  * The file is transferred to the user's home directory `~/`.

* **1. Nginx Installation**
  * [1-install_nginx_web_server](./1-install_nginx_web_server): Bash script to configure a new Ubuntu machine with Nginx.
  * Nginx listens on port 80.
  * Accessing Nginx at `/` returns a page with the text `Hello World` via `curl` GET request.

* **2. Domain Name Setup**
  * [2-setup_a_domain_name](./2-setup_a_domain_name): Text file containing the domain name configured for the server through Gandi.

* **3. Redirection Setup**
  * [3-redirection](./3-redirection): Bash script configuring a new Ubuntu machine with Nginx.
  * Similar to [1-install_nginx_web_server](./1-install_nginx_web_server) with an additional feature: `/redirect_me` location returns a `301 Moved Permanently` redirection.

* **4. Custom 404 Page**
  * [4-not_found_page_404](./4-not_found_page_404): Bash script configuring a new Ubuntu machine with Nginx.
  * Similar to [1-install_nginx_web_server](./1-install_nginx_web_server) with a custom 404 page displaying the text `Ceci n'est pas une page`.

* **5. Custom 404 Page Design**
  * Custom-designed 404 error page accessible at [bdbnb.site/404](http://bdbnb.site/404).

* **6. Efficient Deployment with Fabric**
  * [fabfile.py](./fabfile.py): Python Fabric configuration file defining functions for packaging, deploying, and cleaning up the web app.
    * `pack`: Creates a tar gzipped archive of the current directory.
    * `deploy`: Uploads the archive to the remote server, extracts it, and sets up the application.
    * `clean`: Deletes the archive locally.

These tasks equip me with the essential skills to manage and configure web servers efficiently.
