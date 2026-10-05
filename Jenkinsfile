pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',           
                    url: 'https://github.com/ruchikaborkar01-glitch/node.js-app.git'            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t nodejs-app:latest ./node.js-app'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker rm -f nodejs-app || true'
                sh 'docker run -d -p 3000:3000 --name nodejs-app nodejs-app:latest'
            }
        }

        stage('Verify Container') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
