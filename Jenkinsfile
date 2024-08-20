pipeline {
    agent any
    
    stages {
        stage('Setup') {
            steps {
                bat 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        
        stage('Run') {
            steps {
                bat 'npm run start'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
