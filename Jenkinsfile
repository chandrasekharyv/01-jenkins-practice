pipeline {
    agent {
        node {
           label 'Agent-1'
        }
        
    }
    options {
        ansiColor('xterm')
    }
    environment { 
        USER = "chandu"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
                sh '''
                    ls -ltr
                    pwd
                    echo 'hello jenkins'
                    printenv

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
        stage('Example') {
            environment { 
                AUTH_ACCESS_KEY = credentials('ssh-auth') 
            }
            steps {
                sh 'printenv'
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