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
        
        stage('Copy env') {
            steps {
                sh '''
                sudo cp /root/simple-apps/apps/.env apps/
                '''
            }
        }
        
        stage('Testing Apps') {
            steps {
                sh '''
                cd apps
                npm test
                npm run test:coverage
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
