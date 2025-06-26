pipeline {
    agent any

    stages {
        stage('Install dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest tests'
            }
        }

        stage('Deploy') {
            steps {
                echo '✅ Deployment steps go here (optional)'
            }
        }
    }
}
