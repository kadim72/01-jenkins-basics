pipeline {
    agent any
    environment {
        MYVAR = "123456"
    }

    stages {


        stage('Setup') {
            steps {
                // withCredentials([usernamePassword(credentialsId: 'jenkins-tn', usernameVariable: "myuser", passwordVariable: "mypassword")]) {

                //     sh '''
                //     echo ${myuser}
                //     echo ${mypassword}
                //     '''
                // }

                sh 'echo "${MYVAR}"'
                 echo "-----"
                echo "${MYVAR}"
                echo "-----"
                echo "${JOB_NAME}"
             
                sh "pip install -r requirements.txt"

            
            }
        }
        stage('Test') {
            steps {
                sh "pytest"
                
            }
        }    
        stage('Deployment') {
            input {
                message "Do you want to proceed further?"
                ok "Yes"
            }
            steps {
                echo "Running Deployment"
                
            }
        } 
        
            
    }
}