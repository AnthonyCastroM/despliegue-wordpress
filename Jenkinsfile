pipeline {
    agent any

    stages {
        stage('1. Checkout') {
            steps {
                checkout scm
            }
        }
        stage('2. Detener ambiente (down)') {
            steps {
                sh 'docker compose down'
            }
        }
        stage('3. Levantar ambiente (up)') {
            steps {
                sh 'docker compose up -d'
            }
        }
        stage('4. Validar despliegue (ps)') {
            steps {
                sh 'docker ps'
            }
        }
    }
}