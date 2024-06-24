## We are done with all pre-reuisites. Now let's do a quick demo.

### Create a jenkins pipeline job with below selections:

#### Check the checkbox for **GitHub hook trigger for GITScm polling** so that the building pipeline will start as soon as we make commit on GitHub.

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/7a1a0289-6c59-4b6e-94e2-1cb71159ba57)

#### Add the git repository and branch as shown below

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/cda0888d-fc55-4d6b-b4c8-359409b417f9)

#### Add the file name in which we have written pipeline in Groovy and **Save**

![image](https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline/assets/160045230/a4342e4b-3771-49c8-83fd-b0b45ab8109d)


#### Let's make a commit from our instance 1 and push it to the GitHub repository.


#### As you can see, pushed changes appeared on GitHub repo.


#### This commit triggered the Jenkins pipeline and our job is building.
