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
                sh 'ls'
                withSonarQubeEnv('Sonarqube') {
                    sh 'apt update'
                    sh 'apt install maven'
                    sh "mvn -version"
                    
                }
            }
        }
    }
}