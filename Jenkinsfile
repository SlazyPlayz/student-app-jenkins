pipeline {
    agent any

    stages  {
        stage('Install Packages') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Integration tests') {
            steps {
                sh 'npm test'
            }
        }
    }
}