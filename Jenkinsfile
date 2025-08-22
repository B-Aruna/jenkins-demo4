pipeline {
    agent any 

    environment {
        DOCKER_IMAGE = "arunadocker123/jenkins-demo1"
        DOCKER_TAG = "latest"
        DOCKER_REGISTRY = "docker.io"
        DOCKER_DIGEST = "sha256:a449d2e0b0b2ed78f175d96f41650485ce597400a0db6fb8fd1aa18d5ee282b1"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building Go Application...'
            }
        }

        stage('Docker Build & Push') {
            steps {
                echo 'Building and pushing Docker image...'
                sleep 15
            }
        }


        stage('Test') {
            steps {
                echo 'Running Unit Tests...'
            }
        }

        stage('Deploy') {
            agent any
            steps {
                echo 'Deploying...'
                sleep 10
            }
        }
    }
}
