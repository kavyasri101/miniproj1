pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from version control
                git 'https://github.com/kavyasri101/miniproj1.git'
            }
        }
        
        stage('Build and Test') {
            steps {
                // Build and run tests using Maven
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn clean verify"
                }
            }
        }
        
        stage('SonarQube Analysis') {
            steps {
                // Perform SonarQube analysis
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn sonar:sonar \
                        -Dsonar.projectKey=mks \
                        -Dsonar.projectName='mks' \
                        -Dsonar.host.url=http://localhost:9099 \
                        -Dsonar.login=sqp_52389c3f36217516e7c02f2db787e39eae141d91"
                }
            }
        }
    }
}
