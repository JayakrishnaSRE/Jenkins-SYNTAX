pipeline {
    agent {
        label 'AGEN-1'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!'
            }
        }

        stage('Build') {
            steps {
                echo 'Running build step...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}