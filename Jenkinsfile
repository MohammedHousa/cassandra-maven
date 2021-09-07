pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('Sonarqube') {
                    withMaven(maven:'Maven 3.8.2') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
        }
    }
}