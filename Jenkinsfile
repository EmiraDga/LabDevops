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
    }
}
