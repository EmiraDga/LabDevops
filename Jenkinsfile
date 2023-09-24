pipeline {
    agent any
     
    stages {
        stage('Checkout') {
            steps {
                 echo "check out the project"
            }
        }
        
        stage('Build') {
            steps {
                 echo "Building the project"
            }
        }
    }
    
    post {
        always {
            emailext(
                subject: "Build Notification",
                body: "Build Status: ${currentBuild.result}",
                recipientProviders: [[$class: 'UpstreamCommitterRecipientProvider']],
                to: "arctictestdevops@gmail.com" 
            )
        }
    }
}
