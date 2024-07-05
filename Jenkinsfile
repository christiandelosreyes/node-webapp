pipeline {
    agent {
        label 'linux-node'
        } 

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git branch: 'main', url: 'https://github.com/christiandelosreyes/node-webapp.git'
                }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('christian/node-webapp', '.')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('christian/node-webapp').inside {
                    sh 'docker run -d -p 3000:3000 christian/node-webapp''
    }
    }
    }
    }
    }
}
