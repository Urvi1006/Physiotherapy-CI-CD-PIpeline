pipeline {
    agent any
        
        
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
