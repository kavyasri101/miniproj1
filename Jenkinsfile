pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/username/repo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
                // Add your testing steps here
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
                // Add your deployment steps here
            }
        }
    }
}
