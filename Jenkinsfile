pipeline {
    agent any

    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }

    post {
        always {
            emailext(
                body: 'A Test EMail!!!',
                subject: 'Test',
                to: 'arctictestdevops@gmail.com' 
            )
        }
    }
}
