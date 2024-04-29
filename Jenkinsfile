pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t mywebapp .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8080:80 mywebapp'
            }
        }
    }
}

