pipeline {
    agent any
    stages {
        agent{
            docker{
                image 'maven'
            }
        }
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('Sonarqube') {
                    sh 'ls'
                    sh 'mvn -version'
                    
                }
            }
        }
    }
}