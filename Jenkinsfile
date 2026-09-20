pipeline {
    agent {
        label 'AGEN-1'
    }
    environment {
        APP_NAME = 'myapp'
    stages {
        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!'
                sh '''
                    echo ${APP_NAME}
                '''
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
    post { 
        
        success {
            echo 'This will run only if successful'
        }
        
        failure {
            echo 'This will run only if failed'
        }   
        
        always { 
            echo 'I will always say Hello again!'
        }
    }
}