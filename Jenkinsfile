pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'ls'
                }
            }
        }
    }
}