pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            agent {
                docker {
                    image 'ubuntu'
                }
            }
            steps {
                withSonarQubeEnv('Sonarqube') {
                    sh 'ls'
                    sh 'apt install maven -y'
                    sh 'mvn -version'
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}