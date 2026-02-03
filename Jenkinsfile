pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                dir('spring-boot-2-rest-service-basic') {
                    sh 'mvn clean test'
                }
            }
        }
    }

    post {
        failure {
            echo 'Build failed 💀'
        }
        success {
            echo 'Build passed 🔥'
        }
    }
}
