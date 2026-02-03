pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

    stages {
        stage('Build & Test') {
            steps {
               dir('demo') {
    sh 'mvn clean test'
}
            }
        }
    }

    post {
        always {
            // Publish JUnit test results no matter what
           junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'
        }
        success {
            echo 'Build success 🚀'
        }
        failure {
            echo 'Build failed 💀'
        }
    }
}
