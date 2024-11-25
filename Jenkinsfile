pipeline {
    agent any
    environment {
        DB_HOST = '172.0.0.1'
        USERNAME = "USER1"
        PASSWORD = "password123"

        USERPWD = credentials('userpwd')
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

               
             
                //sh "pip install -r requirements.txt"
                echo "USERPWD : ${USERPWD}"
                echo "USERPWD_USR : ${USERPWD_USR}"
                echo "USERPWD_PSW : ${USERPWD_PSW}"
        

            
            }
        }
        stage('Test') {
            steps {
//                sh "pytest"
                    withCredentials([usernamePassword(credentialsId: 'userpwd',usernameVariable: 'USERNAME',passwordVariable: 'PASSWORD')]) {

                        echo "USERNAME :  ${USERNAME}"
                        echo "PASSWORD :  ${PASSWORD}"
                    }

                
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