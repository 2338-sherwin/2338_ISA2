pipeline {
    agent any
    
    stages {        
        stage('Build Docker Image 2338') {
            steps {
                script {
                    dockerImage = docker.build("2338")
                }
            }
        }

        stage('Create & Run Docker Container 2338') {
            steps {
                script {
                    dockerImage = docker.run("--name 2338 2338")
                }
            }
        }

        stage('Stop Docker Container 2338') {
            steps {
                script {
                    dockerImage = docker.stop("2338")
                }
            }
        }

        stage('Delete Docker Container 2338') {
            steps {
                script {
                    dockerImage = docker.rm("2338")
                }
            }
        }
        
        stage('Create & Run Docker Container 2338') {
            steps {
                script {
                    dockerImage.run("--name 2338 2338")
                }
            }
        }
    }
}
