pipeline {
    agent any

    stages {
        stage('SonarQube analysis') {
            steps{
                withSonarQubeEnv(credentialsId: '54d46da8ad21eef2a1bff91a8310a0558257bbe5', installationName: 'msami2030') { // You can override the credential to be used
                sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
                }
            }
        }
    }
}