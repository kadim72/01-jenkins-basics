pipeline {
    agent any

    stages {
        stage('Setup & Test'){
         
                parallel {

                    "Setup": {
                        steps {
                            echo "Setup ..."
                            sh 'sleep 30'
                        }
                    }

                    "Test": {
                        steps {
                            echo "Test ..."
                            sh 'sleep 30'                    
                        }
                    }   

                }    
               
        }     
    }
}