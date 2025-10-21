pipeline {
    agent any

    stages {
        stage('Declarative: Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Stage Build ignorado para execu��o sem Docker'
            }
        }

        stage('Testes') {
            steps {
                echo 'Executando testes simulados...'
            }
        }

        stage('SonarQube') {
            steps {
                echo 'An�lise SonarQube simulada...'
            }
        }

        stage('Deploy Dev') {
            steps {
                echo 'Deploy Dev simulado...'
            }
        }

        stage('Aprova��o para Produ��o') {
            steps {
                input message: 'Aprovar para Produ��o?', ok: 'Sim'
            }
        }

        stage('Deploy Prod') {
            steps {
                echo 'Deploy Prod simulado...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline finalizada com sucesso!'
        }
        failure {
            echo 'Pipeline falhou.'
        }
    }
}
