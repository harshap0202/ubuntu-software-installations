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

**inventory.ini** - basic syntax
```ini
target-01  ansible_host=xxx.xx.xx.xx  ansible_connection=ssh  ansible_user=harsh   ansible_ssh_pass=temp
# <alias>  <----host ip address---->  <--connection type--->  <---remote user--->  <--login password--->
```

check ansible connection 
```bash
ansible -i inventory target1 -m ping 
```

# Commands to Uninstall Ansible on Ubuntu

```bash
# confirm installed
ansible --version

# uninstall ansible
sudo apt-get remove --purge ansible

# Remove Dependencies and Unused Packages
sudo apt-get autoremove

# confirm uninstalled
ansible --version
```