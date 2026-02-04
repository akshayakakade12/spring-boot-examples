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
        success {
            echo 'Build & tests passed 🎉'
        }
        failure {
            echo 'Build failed 💀'
        }
    }
}

