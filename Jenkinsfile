pipeline {
    agent any
    
    stages {
        stage('Clone Git Repo'){
            steps {
                script {
                    git clone https://github.com/2338-sherwin/2338_ISA2.git
                }
            }
        }
        
        stage('Build Docker Image 2338') {
            steps {
                script {
                    dockerImage = docker.build("2338")
                }
            }
        }

        stage('Delete Docker Container 2338') {
            steps {
                script {

                    dockerImage = docker.run("--name 2338")
                    dockerImage = docker.stop("2338")
                    dockerImage = docker.rm("2338")
                }
            }
        }
        
        stage('Create & Run Docker Container 2338') {
            steps {
                script {
                    dockerImage.run("--name 2338")
                }
            }
        }
    }
}
