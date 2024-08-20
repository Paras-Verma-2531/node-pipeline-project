pipeline {
    agent any
    
    stages {
        stage('Setup') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        
        stage('Run') {
            steps {
                sh 'npm run start'
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
