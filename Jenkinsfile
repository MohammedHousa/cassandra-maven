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
                    sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=54d46da8ad21eef2a1bff91a8310a0558257bbe5'
                }
            }
        }
    }
}