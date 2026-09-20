pipeline {
    agent {
        label 'AGEN-1'
    }
    environment {
        COUSRSE = "myapp"
    }
    options {
        timeout(time: 10, unit: 'SECOND')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!'
                sh '''
                    echo $COUSRSE
                    sleep 5
                    env

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
        
        // success {
        //     echo 'This will run only if successful'
        // }
        
        // failure {
        //     echo 'This will run only if failed'
        // }   
        
        aborted { 
            echo 'pipeline was aborted'
        }
    }
}