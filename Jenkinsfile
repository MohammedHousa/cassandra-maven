pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('Sonarqube2') {
                    sh 'ls'
                }
            }
        }
    }
}