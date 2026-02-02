pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
'
    }

    stages {
        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }
    }

    post {
        failure {
            echo 'Build failed 💀'
        }
        success {
            echo 'Build success 🚀'
        }
    }
}
