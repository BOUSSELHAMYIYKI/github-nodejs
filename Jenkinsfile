pipeline {
    agent any

    tools {
        nodejs 'NodeJS' // nom de ta version NodeJS définie dans Jenkins
    }

    stages {
        stage('Checkout code') {
            steps {
                checkout scm
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        always {
            echo "Pipeline terminé."
        }
    }
}
