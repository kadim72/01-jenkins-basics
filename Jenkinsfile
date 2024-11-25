pipeline {
    agent any
    environment {

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
                sh 'echo "${JOB_NAME}"'
                echo "-----"
                echo "${JOB_NAME}"
                sh 'printenv'
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