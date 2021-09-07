pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            agent {
                docker {
                    image 'maven'
                }
            }
            steps {
                withSonarQubeEnv('Sonarqube') {
                    sh 'ls'
                    sh 'mvn -version'
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}