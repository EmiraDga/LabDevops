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
            emailext body: 'Hello from jenkins', subject: 'Test email', to: 'arctictestdevops@gmail.com'
        }
        failure{
            emailext body: 'email sent out from jenkins', subject: 'Test email FAILED!!!', to: 'arctictestdevops@gmail.com'
        }
    }
}
