pipeline {
    agent any
    stages {
        stage('build && SonarQube analysis') {
            steps {
                sh 'ls'
                withSonarQubeEnv('Sonarqube') {
                    sh 'apt install maven'
                    sh 'mvn clean package sonar:sonar'
                    
                }
            }
        }
        stage("Quality Gate") {
            steps {
                timeout(time: 1, unit: 'HOURS') {
                    // Parameter indicates whether to set pipeline to UNSTABLE if Quality Gate fails
                    // true = set pipeline to UNSTABLE, false = don't
                    waitForQualityGate abortPipeline: true
                }
            }
        }
    }
}