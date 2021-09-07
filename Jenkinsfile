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
                sh 'ls'
                sh 'mvn clean package sonar:sonar -Dsonar.host.url=http://34.226.190.81:9000 -Dsonar.login=3d8ee63df4fff05299b63326167df65acd23890d'
            }
        }
    }
}