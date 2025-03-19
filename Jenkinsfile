pipeline {
    agent any

    environment {
        IMAGE_NAME = "kanishkharamesh/my-app"
        REGISTRY = "docker.io"
        APP_DIR = "/home/vboxuser/Desktop/Jenkins"
        DOCKER_USER = "kanishkharamesh"          // Replace with your Docker Hub username
<<<<<<< HEAD
<<<<<<< HEAD
        DOCKER_PASS = "ka12@2003"          // Replace with your Docker Hub password
=======
        DOCKER_PASS = "ka12@20033"          // Replace with your Docker Hub password
>>>>>>> 7180f88 (updated)
=======
        DOCKER_PASS = "ka12@2003"          // Replace with your Docker Hub password
>>>>>>> e05bb2f (Added Jenkinsfile)
    }

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/Kanishkharamesh/Jenkins.git', branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh "docker build -t $IMAGE_NAME:latest ."
                }
            }
        }

        stage('Login to Docker Registry') {
            steps {
                script {
                    sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }

        stage('Push Image to Docker Registry') {
            steps {
                script {
                    sh "docker push $IMAGE_NAME:latest"
                }
            }
        }

        stage('Deploy using Docker Compose') {
            steps {
                script {
                    sh "docker-compose up -d"
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check the logs for errors.'
        }
    }
}
