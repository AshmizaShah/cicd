pipeline {
    agent { label 'node1linux' }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository from GitHub using SSH credentials
                git credentialsId: 'cicd', url: 'git@github.com:AshmizaShah/cicd.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                // Execute the build step (assuming hello.py is in the repository root)
                sh 'python3 hello.py'
            }
        }
    }
}
