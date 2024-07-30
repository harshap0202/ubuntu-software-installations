# Commands to install Ansible on Ubuntu

> Note: python is required for ansible 

```bash
sudo apt update

# to ensure that the official project’s PPA is included in system’s list of apt sources
sudo apt-add-repository ppa:ansible/ansible

sudo apt update

sudo apt install ansible -y
```

## Inventory File Syntax : 

```bash
# inventory.ini
    └─> $ target1  ansible_host=192.168.232  ansible_connection=ssh   ansible_user=harsh  ansible_ssh_pass=temp
#         <alias>  <-- host ip address -->   <-- connection type -->  <--remote user -->  <-- login password -->

# check ansible connection 
    └─> $ ansible -i inventory target1 -m ping 
```
