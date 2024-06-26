## Pre-requisites for the project are given below:

### Two Instances created with minimal specifications (we took ubuntu, t2.micro):

  **Instance 1 will have Git and Jenkins**

  Update the instance first (best practice)

    sudo apt update -y

  Use below commands to install

  **Git** (mostly it's already installed, if not present):

      sudo apt install git-all                   # skip this if present
      git --version                              # to check version
      git init                                   # to initialize the git repo
      
      # OR Directly clone the repo.
      
      git clone <repository-url>                 # to clone remote repo to local

  **Jenkins:**

      sudo apt update -y
      sudo apt install openjdk-17-jdk -y
      curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
        /usr/share/keyrings/jenkins-keyring.asc > /dev/null
      echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
        https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
        /etc/apt/sources.list.d/jenkins.list > /dev/null
      sudo apt-get update -y
      sudo apt-get install jenkins -y
      sudo systemctl daemon-reload
      sudo systemctl enable jenkins
      sudo systemctl start jenkins
      sudo systemctl status jenkins

  ![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/d22b0582-b825-4707-b206-a3258411d48c)

  Setup Jenkins by installing reuired plugins, creating user credentials.

  **Instance 2 will have Java and Docker**

  Update the instance first (best practice)

    sudo apt update -y

  Use below commands to install

  **Java:**

    sudo apt install openjdk-17-jdk -y

  **Docker:**

    sudo apt install docker.io -y

  ![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/27b0d356-d626-4f96-b212-608b58c487a9)


### Add the instance 2 as a Node in Jenkins as shown below

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/32ced10f-9c6a-4db5-bc59-5b73230bcc60)

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/5860a245-0fb0-4a78-81a6-3ba3aa7af1c2)

### Add your DockerHub credentials so that we can push the image on DockerHub

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/efd403ae-aaed-4dfd-b848-ed7dca5670f6)

### Setup GitHub Webhook

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/52cfa422-f2e3-4e6f-97ae-102581bdb4bd)

### To run a python application, we will need some libraries which are given below. I have mentioned that in requirements.txt file.

   *Flask==2.0.1: Flask is a popular Python web application framework used for building web apps.*
 
   *Werkzeug==2.0.1: Werkzeug is a WSGI (Web Server Gateway Interface) utility library that Flask depends on internally.*

## Here we completed our pre-requisites.
