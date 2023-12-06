pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your GitHub repository
                git 'https://github.com/your-username/your-repo.git'
            }
        }
        
        stage('Build') {
            steps {
                // Add your build steps here
                // For example, running tests, compiling code, etc.
                sh 'your_build_command'
            }
        }
        
        stage('Deploy') {
            steps {
                // Add your deployment steps here
                // For example, deploying to a server, pushing to production, etc.
                sh 'your_deploy_command'
            }
        }
    }
    
    post {
        success {
            // Actions to perform when the build succeeds
            echo 'Build successful!'
        }
        failure {
            // Actions to perform when the build fails
            echo 'Build failed!'
        }
    }
}
