pipeline {
    agent {
        node {
           label 'Agent-1'
        }
        
    }
    options {
        ansiColor('xterm')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
                sh '''
                    ls -ltr
                    pwd
                    echo 'hello jenkins'

                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying......'
                // error 'job is failure'
            }
        }
    }

    post { 
        always { 
            echo 'I will always run job is success or not !'
        }
        success {
            echo 'i will run when the job is success'
        }
        failure {
            echo 'it will run when job is failure'
        }
    }
}