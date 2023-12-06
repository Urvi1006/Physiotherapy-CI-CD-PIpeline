pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your GitHub repository
                git 'https://github.com/Urvi1006/Physiotherapy-website.git'
            }
        }
        
        stage('HTML Validation') {
            steps {
                // Validate HTML using the W3C Markup Validation Service
                sh 'curl -H "Content-Type: text/html; charset=utf-8" --data-binary "@index.html" https://validator.w3.org/nu/?out=gnu'
            }
        }
        
        stage('Deploy') {
            steps {
                // Copy HTML/CSS files to the deployment directory
                sh 'mkdir public'
                sh 'cp -r * public/'
            }
        }
    }
    
    post {
        success {
            // Actions to perform when the deployment succeeds
            echo 'Deployment successful!'
        }
        failure {
            // Actions to perform when the deployment fails
            echo 'Deployment failed!'
        }
    }
}
