pipeline {
    agent any
     
    stages {
        stage('Checkout') {
            steps {
                // Check out your source code repository here
            }
        }
        
        stage('Build') {
            steps {
                // Build your project
            }
        }
    }
    
    post {
        always {
            emailext(
                subject: "Build Notification",
                body: "Build Status: ${currentBuild.result}",
                recipientProviders: [[$class: 'UpstreamCommitterRecipientProvider']],
                to: "arctictestdevops@gmail.com" // Replace with recipient's email
            )
        }
    }
}
