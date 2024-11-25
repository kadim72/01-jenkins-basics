pipeline {
    agent any

    stages {
        parrallel {

            stage('Setup') {
                steps {
                    echo "setup ..."
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