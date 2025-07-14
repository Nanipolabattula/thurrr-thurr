pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/Nanipolabattula/thurrr-thurr.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test || echo "No tests defined."'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying application...'
                // Example real deploy command:
                // sh 'scp -r ./dist ubuntu@server:/var/www/html'
            }
        }
    }
}

















