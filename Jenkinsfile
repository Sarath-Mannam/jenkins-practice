pipeline {
    agent { node { label 'Agent-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ls -ltr'     // I want to undersand what are the files 
                sh 'pwd'         // I want to know what is the working directory
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // error 'this is failed'
            }
        }
    }

    post { 
        always { 
            echo 'I will always run whether job is success or not'
        }
        success {
            echo 'I will run only when job is success'
        }
        failure {
            echo 'I will run only when job is failed'
        }
    }
}