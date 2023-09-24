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
            echo "Build succeeded! This will run on successful build."
        }
    }
}
