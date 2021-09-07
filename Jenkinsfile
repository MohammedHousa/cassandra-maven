pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('Sonarqube') {
                    sh 'ls'
                    sh 'apt update -y'
                    sh 'apt install maven -y'
                    sh 'mvn -version'
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}