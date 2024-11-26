pipeline {
    agent any

    parameters {
        string(name: 'ENVIRONMENT', defaultValue: 'dev', description: 'give the environment')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: "run test pipeline")
    }

    stages {
       

                    stage("Setup") {
                        steps {
                            echo "Setup ..."
                            sh 'sleep 30'
                        }
                    }

                    stage("Test") {
                        steps {
                            echo "Test ..."
                            sh 'sleep 30'                    
                        }
  
        
                    stage('deploy') {
                        when {
                            parameters {
                                params.RUN_TESTS == true
                            }
                        }
                        steps {
                            echo  "deploying in env : ${params.ENVIRONMENT}"
                        }

                    }
        }  
           
    }     
}
