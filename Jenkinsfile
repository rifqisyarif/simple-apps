pipeline {
    agent {
        node {
            label 'devops-rifqi'
        }
    }

    stages {
        stage('Build Apps') {
            steps {
                echo "Proses build apps"
            }
        }
    }
    
    stages {
        stage('Testing Apps') {
            steps {
                echo "Proses test apps"
            }
        }
    }
    
    stages {
        stage('Scanning Code') {
            steps {
                echo "Proses scanning apps"
            }
        }
    }
    
    stages {
        stage('Dockerized') {
            steps {
                echo "Proses dockerized apps"
            }
        }
    }
    
    stages {
        stage('Deploying Apps') {
            steps {
                echo "Proses deploy apps"
            }
        }
    }
    
    stages {
        stage('Publish Image') {
            steps {
                echo "Proses publish apps"
            }
        }
    }
    
}
