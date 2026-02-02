pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

    stages {
        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }
    }

    post {
        always {
            // This runs no matter what
            junit 'target/surefire-reports/*.xml'
        }
        success {
            echo 'Build success 🚀'
        }
        failure {
            echo 'Build failed 💀'
        }
    }
}
