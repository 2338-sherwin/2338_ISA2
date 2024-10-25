pipeline {
    agent any
    
    stages {        
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sher4win/2338 .'
            }
        }

        stage('Create Docker Container 2338') {
            steps {
                bat 'docker run --name 2338 sher4win/2338'
            }
        }

        stage('Stop Docker Container 2338') {
            steps {
                bat 'docker stop 2338'
            }
        }

        stage('Delete Docker Container 2338') {
            steps {
                bat 'docker rm 2338'
            }
        }

        stage('Create & Run Docker Container 2338') {
            steps {
                bat 'docker run --name 2338 sher4win/2338'
            }
        }
    }
}
