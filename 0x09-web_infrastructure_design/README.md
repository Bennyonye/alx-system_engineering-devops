# Web Infrastructure Design

This project, part of the **ALX Full Stack Software Engineering curriculum**, focuses on understanding the design principles of a web infrastructure.

## Key Concepts
* Fundamentals of networking
* Server architecture
* Web servers
* Application servers
* DNS and its record types
* Load balancers
* Monitoring techniques
* Database management
* Single points of failure mitigation
* HTTP and HTTPS protocols
* Firewall configurations

## File Descriptions

Each file contains a link to an image hosted on Imgbox, depicting a design based on specific requirements:

### [0-simple_web_stack](0-simple_web_stack)

Designs a basic one-server web infrastructure hosting a website accessible via `www.foobar.com`.

Components:
* 1 physical server
* 1 Nginx web server
* 1 application server
* 1 set of application files
* 1 MySQL database
* Domain name `foobar.com` configured with a `www` record pointing to server IP `8.8.8.8`

### [1-distributed_web_infrastructure](1-distributed_web_infrastructure)

Expands on the previous design to include three servers hosting the website `www.foobar.com`.

Additional Components:
* 2 physical servers
* 1 Nginx web server
* 1 application server
* 1 HAproxy load balancer
* 1 set of application files
* 1 MySQL database

### [2-secured_and_monitored_web_infrastructure](2-secured_and_monitored_web_infrastructure)

Enhances the previous design with security measures, encrypted traffic support, and monitoring capabilities.

Additional Components:
* 3 firewalls
* SSL certificate for HTTPS encryption
* 3 monitoring clients

### [3-scale_up](3-scale_up)

Further scales up the infrastructure to accommodate increased traffic and redundancy.

Additional Components:
* 1 physical server
* 1 HAproxy load balancer configured as a cluster with the existing one
* Segmented components (web server, application server, database) each with dedicated servers

## Files

| Filename | Description |
| -------- | ----------- |
| [`0-simple_web_stack`](./0-simple_web_stack)  | Design of a LAMP stack web infrastructure with 1 server, 1 web server, 1 application server, 1 database, and 1 domain name |
| [`1-distributed_web_infrastructure`](./1-distributed_web_infrastructure) | Enhanced web infrastructure design with additional components including load balancer |
| [`2-secured_and_monitored_web_infrastructure`](2-secured_and_monitored_web_infrastructure) | Secure and monitored web infrastructure design with firewalls, SSL certificate, and monitoring clients |
| [`3-scale_up`](3-scale_up) | Further scaled-up web infrastructure design with additional server and load balancer configuration |
