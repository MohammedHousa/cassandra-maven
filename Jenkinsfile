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
                withSonarQubeEnv('sonarqube') {
                    sh 'ls'
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}