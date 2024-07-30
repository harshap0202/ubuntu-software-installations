# Commands to uninstall Virtual-Box on Ubuntu

```bash
sudo apt purge virtualbox

sudo apt purge virtualbox-dkms 
```

# Commands to install Virtual-Box on Ubuntu

```bash
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -

wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -

sudo apt install software-properties-common

echo "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian $(lsb_release -sc) contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list

sudo apt update

sudo apt install virtualbox-7.0

virtualbox
```