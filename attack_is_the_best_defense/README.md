# Attack is the best defense

## Tools

* Wireshark
* Telnet
* Tcpdump
* Docker
* Hydra

## 0-0-sniffing

### Overview

Security, especially network security, is crucial in today's digital landscape. However, despite advancements, there are still vulnerabilities, such as unencrypted communication channels like Telnet. In this project, we'll explore sniffing unencrypted traffic using tools like `tcpdump` to uncover sensitive information like passwords.

### Task

You're provided with a script, `user_authenticating_into_server`, which simulates authentication over Telnet. Your objective is to execute this script locally and sniff the network traffic using `tcpdump` to find the password being transmitted.

### Solution

* The password encoded in ASCII: `bXlwYXNzd29yZDk4OTgh7`
* Username: `mylogin`

### Sniffed Packet

```packet
  0000   d8 b6 b7 a1 1f 63 cc b0 da 2a bf b6 08 00 45 10   .....c...*....E.
0010   00 4a 40 f2 40 00 40 06 62 67 c0 a8 01 07 12 c5   .J@.@.@.bg......
0020   c2 d0 b5 12 02 4b 67 8b 60 d1 67 35 59 20 80 18   .....Kg.`.g5Y ..
0030   01 f5 a3 88 00 00 01 01 08 0a 21 35 2c 39 b2 84   ..........!5,9..
0040   5c 4c 62 58 6c 77 59 58 4e 7a 64 32 39 79 5a 44   \LbXlwYXNzd29yZD
0050   6b 34 4f 54 67 68 0d 0a                           k4OTgh..
```

## 1-dictionary_attack

Password-based authentication systems are vulnerable to dictionary attacks. Let's perform one on an SSH account.

### Steps

1. Install Docker on your Ubuntu Vagrant machine.
2. Pull and run the Docker image `sylvainkalache/264-1` using the command: `docker run -p 2222:22 -d -ti sylvainkalache/264-1`.
3. Obtain a password dictionary.
4. Install Hydra and use it to brute force the SSH account `sylvain` on the Docker container.
5. Since the Docker container is local, use IP `127.0.0.1` and port `2222`.
6. The password length is 11 characters.

With these steps, you can attempt to break into the SSH account using Hydra.
