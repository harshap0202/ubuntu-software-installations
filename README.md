# Ubuntu Software Installations

This git repo consists a step by step process for installation of various softwares in ubuntu

## Index: 
 - [Ansible](ansible.md)
 - [Docker](docker.md)
 - [Jenkins](jenkins.md)
 - [Kubernetes](kubernetes.md)
 - [Shell](shell.md)
 - [SSH Setup](ssh-setup.md)
 - [Terraform](terraform.md)
 - [VirtualBox](virtualbox.md)

---
---

## Other Linux Distributions and Package Managers

Linux boasts a diverse range of distributions, each with its own package management system and installation tools.

This repository includes commands and instructions specifically for Ubuntu. However, you can adapt these commands for other distributions as needed. Below is a list of popular Linux distributions along with their associated package managers and installation tools for your reference:


| **Package Manager** | **Distributions**                                  |
|---------------------|----------------------------------------------------|
| **apt**             | Ubuntu, Debian, Linux Mint, elementary OS          |
| **yum**             | Red Hat Enterprise Linux (RHEL), CentOS            |
| **dnf**             | Fedora, CentOS Stream, RHEL 8 and later            |
| **zypper**          | openSUSE, SUSE Linux Enterprise                    |
| **pacman**          | Arch Linux, Manjaro, EndeavourOS                   |


For a simple test of commands, here's how you would install `htop` using each of the package managers:

- **apt** -> 
  ```bash
  sudo apt update
  sudo apt install htop
  ```

- **yum** -> 
  ```bash
  sudo yum check-update
  sudo yum install htop
  ```

- **dnf** -> 
  ```bash
  sudo dnf check-update
  sudo dnf install htop
  ```

- **zypper** -> 
  ```bash
  sudo zypper refresh
  sudo zypper install htop
  ```

- **pacman** -> 
  ```bash
  sudo pacman -Syu
  sudo pacman -S htop
  ```

> You can run `htop` in your terminal after installation to view and manage system processes interactively.