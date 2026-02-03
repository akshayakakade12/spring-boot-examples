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
            junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'
        }
        success {
            echo 'Build passed 😎'
        }
        failure {
            echo 'Build failed 💀'
        }
    }
}
