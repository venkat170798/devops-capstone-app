pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "venkatr271/devops-app"
        CONTAINER_NAME = "devops-container"
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/venkat170798/devops-capstone-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker rm -f $CONTAINER_NAME || true'
                sh 'docker run -d -p 80:3000 --name $CONTAINER_NAME devops-app'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                sh 'docker tag devops-app $DOCKER_IMAGE'
                sh 'docker push $DOCKER_IMAGE'
            }
        }
    }
}
