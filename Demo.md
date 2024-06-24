## We are done with all pre-reuisites. Now let's do a quick demo.

### Create a Jenkinsfile for pipeline. You can refer the file tagged as *Jenkinsfile*.

### Create a jenkins pipeline job with below selections:

#### Check the checkbox for **GitHub hook trigger for GITScm polling** so that the building pipeline will start as soon as we make commit on GitHub.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/7a1a0289-6c59-4b6e-94e2-1cb71159ba57)

#### Add the git repository and branch as shown below

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/cda0888d-fc55-4d6b-b4c8-359409b417f9)

#### Add the file name in which we have written pipeline in Groovy and **Save**

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/a4342e4b-3771-49c8-83fd-b0b45ab8109d)

### Let's make a commit from our instance 1 and push it to the GitHub repository.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/88d50c6c-6892-4bdc-882e-5e204d6b0efa)

### As you can see, pushed changes appeared on GitHub repo.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/7dfd0191-8037-4078-b115-d426d2faeb68)

### This commit immediately triggered the Jenkins pipeline and our job is building.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/e4781181-3b6e-4af9-b543-d3f927ed7c6f)

### If everything is good, & it should be, our job will build successfully

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/c87c3e24-e904-4be8-8f52-3f82318c08bc)

### You can check the status in "Console Output""

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/39aad492-c0d1-4d71-bab1-6cef72d6815c)

### You can verify on the slave node i.e. our instance 2 which we have added as node in Jenkins.

### Whole Git repository got cloned on slave node and as you can see, image and container also got created and container is up.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/920b393b-4516-4da1-bca3-10f96fd33b8c)

### In the next stage, it is pushing image to Docker Hub. Our image got pushed on the Docker Hub.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/f8ab4711-509c-451d-a0d5-f51ba2c1d439)

### Let's confirm if the application is running on given port i.e. 5000 by copying <Public-IP>:<5000> on browser.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/f96b933a-c25b-4b63-9af3-382cda48bd4c)

## We can see the output, our application is working fine !!!
