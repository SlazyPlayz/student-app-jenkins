pipeline {
    agent any

    stages  {
        stage('Install Packages') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Integration Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Start App') {
            steps {
                sh 'npm start &'
            }
        }
        stage('Deploy to production') {
            steps {
                script {
                    input('Deploy to production?')
                }
                echo 'Deploying..'
            }
        }
    }
}