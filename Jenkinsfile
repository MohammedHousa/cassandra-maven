pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('sonarqube2') {
                    sh 'ls'
                }
            }
        }
    }
}