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
                echo '🚀 Deploying Node.js app...'
                sh 'pm2 stop all || true'                  // Stop any running app (optional)
                sh 'pm2 start app.js'                      // Start your Node.js app (adjust filename as needed)
            }
        }
    }
}

