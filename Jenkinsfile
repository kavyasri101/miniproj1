pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from version control
                git 'https://github.com/kavyasri101/miniproj1.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Run automated tests
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy the application (this might vary depending on your specific deployment process)
                // For example, if you're deploying to a web server, you might use something like SCP or FTP
                sh  'scp C:\\Users\\mkavy\\Desktop\\my-app'

            }
        }
    }
}
