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
                sh 'sleep 1'
            }
        }

        stage("Test") {
            steps {
                echo "Test ..."
                sh 'sleep 1'                    
            }

        }

        stage('deploy') {
            // when {
            //     expression {
            //         params.RUN_TESTS == true
            //     }
            // }

            input {
                message "veux tu deployer"
                ok "Oui, deploie"
            }
            steps {
                echo  "deploying in env : ${params.ENVIRONMENT}"
            }

        }
    }  
           
}     

