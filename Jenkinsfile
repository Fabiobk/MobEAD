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
                echo 'Stage Build ignorado para execução sem Docker'
            }
        }

        stage('Testes') {
            steps {
                echo 'Executando testes simulados...'
            }
        }

        stage('SonarQube') {
            steps {
                echo 'Análise SonarQube simulada...'
            }
        }

        stage('Deploy Dev') {
            steps {
                echo 'Deploy Dev simulado...'
            }
        }

        stage('Aprovação para Produção') {
            steps {
                input message: 'Aprovar para Produção?', ok: 'Sim'
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
