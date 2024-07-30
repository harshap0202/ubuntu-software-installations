# Commands to Setup SSH Ubuntu Virtual Machine

This shows connecting local device [Device 1] to a virtual machine [Device 2]

**Setup -**
 - Device 1 is going to ssh into Device 2
 - Device 2 is a virtual machine running on VirtualBox app
 - Device 2 is missing openssh

**Device 2**
---
```bash
sudo apt-get update
sudo apt-get install openssh-server

sudo systemctl enable ssh
sudo systemctl start ssh

ip addr # get ip address from here
```

**Device 1**
```bash
# ssh <username>@<ip> 
  ssh harsh@192.168.11.22

# run a particular command on remote device
ssh username@ip -t command




```