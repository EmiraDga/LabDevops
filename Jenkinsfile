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
                subject: "Commit Notification",
                body: "A commit has occurred in your project.",
                to: "arctictestdevops@gmail.com" // Replace with the recipient's email
            )
        }
    }
}
