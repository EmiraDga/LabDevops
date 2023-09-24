pipeline {
    agent any
     
    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
        
        stage('Email Notification') { 
            steps {
                script {
                    emailext(
                        body: 'A Test EMail',
                        subject: 'Test',
                        to: 'arctictestdevops@gmail.com' 
                    )
                }
            }
        }
    }
}
