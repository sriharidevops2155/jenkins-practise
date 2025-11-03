pipeline {   //Here pipeline is the root element
    agent {
        label 'AGENT-1'
    }
    environment{
        COURSE = 'Jenkins' 
    }

    //Build
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello Build"
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps {
              script{
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
              script{
                    echo 'Deploying..'
                }
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