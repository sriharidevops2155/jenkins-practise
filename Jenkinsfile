pipeline {   //Here pipeline is the root element
    agent {
        label 'AGENT-1'
    }

    //Build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'I will say Hello success'
        }
        failure { 
            echo 'I will say Hello Failure'
        }

    }
}