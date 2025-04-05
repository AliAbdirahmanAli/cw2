pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'Abdirahman'
        SONAR_LOGIN = 'sqa_c6f3c87c6ba4cca30ddcd01dbfe4841ab9a28858'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/AliAbdirahmanAli/cw2.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('Abdirahman') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=Abdirahman -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_c6f3c87c6ba4cca30ddcd01dbfe4841ab9a28858'
                }
            }
        }
    }
}
