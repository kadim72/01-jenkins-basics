pipeline {
    agent any
    environment {
        MYVAR="123456"
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
                sh "echo ${JOB_NAME}"
                echo "${MYVAR}"
                echo "-----"
                echo "${JOB_NAME}"
                sh 'printenv'
                sh "pip install -r requirements.txt"

            
            }
        }
        stage('Test') {
            steps http://127.0.0.1:8080/job/flask-with-pipeline/build?token=testtoken{
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