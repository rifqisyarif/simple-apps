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
                sh '''
                cd apps
                sonar-scanner   -Dsonar.projectKey=Simple-Apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.2.42:9000   -Dsonar.login=sqp_e473107d116e474ffca9b2dda681acf688778429
                '''
            }
        }

        stage('Dockerized') {
            steps {
                sh '''
                docker compose build
                '''
            }
        }

        stage('Deploying Apps') {
            steps {
                sh '''
                docker compose up -d
                '''
            }
        }

        stage('Publish Image') {
            steps {
                echo "Proses publish apps"
            }
        }

    }

}
