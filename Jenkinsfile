// Atualização para rodar pipeline sem lint

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t mobead-app-dev .'
            }
        }

        stage('Testes') {
            steps {
                sh 'docker run mobead-app-dev npm test'
            }
        }

        stage('SonarQube') {
            steps {
                sh 'sonar-scanner'
            }
        }

        stage('Deploy Dev') {
            steps {
                sh './deploy-dev.sh'
            }
        }

        stage('Aprovação para Produção') {
            steps {
                input 'Liberar deploy para produção?'
            }
        }

        stage('Deploy Prod') {
            steps {
                sh './deploy-prod.sh'
            }
        }
    }
}
