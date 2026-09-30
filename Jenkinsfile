pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting latest code from GitHub'
                checkout scm
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website'
                sh 'sudo cp index.html /var/www/html/index.html'
            }
        }

        stage('Verify') {
            steps {
                sh 'curl http://localhost'
            }
        }
    }
}
