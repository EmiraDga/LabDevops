pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the project"
            }
        }
    }

    post {
        success {
            emailext subject: "Commit Notification",
                     body: "A commit event has occurred in the Jenkins pipeline.",
                     to: "arctictestdevops@gmail.com", 
                     recipientProviders: [[$class: 'CulpritsRecipientProvider']]
        }
        failure{
            emailext body: 'email sent out from jenkins', subject: 'Test email FAILED!!!', to: 'arctictestdevops@gmail.com'
        }
    }
}
