pipeline {
    agent any

    stages {
        stage ('Setup & Test'){
            parrallel {

                stage('Setup') {
                    steps {
                        echo "Setup ..."
                        sh 'sleep 30'
                    }
                }

                stage('Test') {
                    steps {
                        echo "Test ..."
                        sh 'sleep 30'                    
                    }
                }   

            }        
        }     
    }
}