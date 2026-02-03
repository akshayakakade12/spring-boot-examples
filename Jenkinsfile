pipeline {
    agent any

    stages {
        stage('Find POM') {
            steps {
                sh 'pwd'
                sh 'ls'
                sh 'find . -name pom.xml'
            }
        }
    }
}
