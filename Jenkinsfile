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
                    sh 'apt update'
                    sh 'apt install maven'
                    sh "mvn -version"
                    
                }
            }
        }
    }
}