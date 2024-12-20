# Commands to install Jenkins Directly on Ubuntu

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins -y

# start jenkins
sudo systemctl start jenkins.service

# check jenkins status
sudo systemctl status jenkins.service
```

### possible errors after Installation

```bash
$ sudo systemctl start jenkins.service

Job for jenkins.service failed because the control process exited with error code.
See "systemctl status jenkins.service" and "journalctl -xeu jenkins.service" for details.
```

```bash
$ sudo systemctl status jenkins.service

× jenkins.service - Jenkins Continuous Integration Server
     Loaded: loaded (/usr/lib/systemd/system/jenkins.service; enabled; preset: enabled)
     Active: failed (Result: exit-code)
    Process: 2129 ExecStart=/usr/bin/jenkins (code=exited, status=1/FAILURE)
   Main PID: 2129 (code=exited, status=1/FAILURE)
        CPU: 10ms
```

### Solution -> Make sure Java is installed on the device using command

    `java --version`

If java is missing, install using the commands on the Java Installation page below

> [Java-Installation-Steps](java.md)


# Commands to install Jenkins on Ubuntu using Docker

NOTE
 - Make sure docker is installed 
 
    `docker --version`

 - pull and run latest stable jenkins image 
  
    `docker run -p 8080:8080 -p 5000:5000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts`

 - at the end you will get a password generated, copy it

 - in browser go to -> localhost:8080

 - paste the generated password there

 - install suggested plugins

 - either skip and continue as admin OR create appropriate users
