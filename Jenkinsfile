

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "here is the checkout"
             
            }
        }

        stage('Send Email') {
            steps {
                script {
                    def fileContent = readFile('README.txt')

                    emailext (
                        subject: 'Nouveau commit dans le dépôt',
                        body: fileContent,
                        to: 'arctictestdevops@gmail.com',
                        attachLog: true,
                        mimeType: 'text/plain'
                    )
                }
            }
        }
    }
}
