pipeline {
    agent {
        node {
            label 'devops-rifqi'
        }
    }

    stages {
        stage('Build Apps') {
            steps {
                sh '''
                cd apps
                npm install
                '''
            }
        }
        
        stage('Testing Apps') {
            steps {
                sh '''
                cd apps
                npm test
                npm test:coverage
                '''
            }
        }

        stage('Scanning Code') {
            steps {
                echo "Proses scanning apps"
            }
        }

        stage('Dockerized') {
            steps {
                echo "Proses dockerized apps"
            }
        }

        stage('Deploying Apps') {
            steps {
                echo "Proses deploy apps"
            }
        }

        stage('Publish Image') {
            steps {
                echo "Proses publish apps"
            }
        }

    }

}
