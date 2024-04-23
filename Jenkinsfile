pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/sanguleumesh007/CI-CD-pipeline.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install' // Assuming it's a Node.js project
            }
        }
        
        stage('Test') {
            steps {
                sh 'npm test' // Assuming npm test runs your tests
            }
        }
    }
    
    post {
        always {
            junit '**/target/surefire-reports/*.xml' // Assuming test results are in this location
        }
    }
}
