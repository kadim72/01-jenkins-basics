pipeline {
    agent any
    environment {
        DB_HOST = '172.0.0.1'
        USERNAME = "USER1"
        PASSWORD = "password123"
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

               
             
                sh "pip install -r requirements.txt"
        

            
            }
        }
        stage('Test') {
            steps {
                sh "pytest"
                echo "The database IP is : ${env.DB_HOST}"
                echo "USER is : ${USERNAME}"
                echo "PASSWORD is : ${PASSWORD}"
                sh 'printenv'
                
            }
        }    
        // stage('Deployment') {
        //     input {
        //         message "Do you want to proceed further?"
        //         ok "Yes"
        //     }
        //     steps {
        //         echo "Running Deployment"
                
        //     }
        // } 
        
            
    }
}