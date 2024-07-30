# Commands to install Jenkins Directly on Ubuntu

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins
```

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
