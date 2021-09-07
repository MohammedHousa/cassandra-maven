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
                    sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar -Dsonar.password '
                }
            }
        }
    }
}