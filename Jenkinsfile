pipeline {
    agent {
        label "Slave1"
    }
    stages {
        stage ("Code Cloning") {
            steps {
                echo "We are cloning the code from GitHub"
                git url:"https://github.com/ajaydabe/Streamlined-Python-Flask-Deployment-using-Docker-CI-CD-Pipeline.git", branch: "main"
            }
        }
        stage ("Build Image") {
            steps {
                echo "Building Image from code"
                sh "docker build -t ajaydabe/pythonpro ."
            }
        }
        stage ("Push image to DockerHub") {
            steps {
                echo "Push docker image to DockerHub"
                withCredentials([usernamePassword(credentialsId: 'DockerHub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    sh 'docker login -u $USERNAME -p $PASSWORD'
                    sh 'docker push ajaydabe/pythonpro'
                    }
                }
            }
        stage ("Run container") {
            steps {
                echo "Run docker image container"
                sh "docker run -itd -p 5000:5000 ajaydabe/pythonpro"
            }
        }
    }
}
