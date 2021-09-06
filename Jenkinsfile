pipeline {
    agent any

    stages {
        stage('Security Scan') {
            steps {
                echo 'Security Scan'
                sh '''
                mvn sonar:sonar \
                    -Dsonar.host.url=http://localhost:9000 \
                    -Dsonar.login=54d46da8ad21eef2a1bff91a8310a0558257bbe5
                '''
            }
        }
    }
}