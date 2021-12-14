pipeline {  
   agent any
   stages {         
     stage('Install Dependencies') { 
       steps {
         // slackSend channel: 'devops', message: 'Job Started' 
         slackSend channel: 'devops', message: "$JOB_NAME Job Started"
         sh 'echo "Install Dependencies..."' 
         sh 'sleep 80' 
       }
       post { 
         always {
           echo "+++++ ALWAYS ++++"             
         }
         success {
           echo "+++++ success ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN SUCCESSFULLY COMPLETED"              
         }
         failure {
           echo "+++++ failure ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN FAILED"             
         }
       }       
     }
     
     stage('Test') { 
       steps {
         // slackSend channel: 'devops', message: 'Testing' 
         slackSend channel: 'devops', message: "$JOB_NAME Testing"            
         sh 'echo "testing application..."'
         sh 'sleep 80'         
       }
       post { 
         always {
           echo "+++++ ALWAYS ++++"             
         }
         success {
           echo "+++++ success ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN SUCCESSFULLY COMPLETED"              
         }
         failure {
           echo "+++++ failure ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN FAILED"             
         }
       }       
     }

     stage("Deploy application") { 
       steps {
         // slackSend channel: 'devops', message: 'Deploying' 
         slackSend channel: 'devops', message: "$JOB_NAME Deploying"            
         sh 'echo "deploying application..."'
         sh 'sleep 80'         
       }
       post { 
         always {
           echo "+++++ ALWAYS ++++"             
         }
         success {
           echo "+++++ success ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN SUCCESSFULLY COMPLETED"              
         }
         failure {
           echo "+++++ failure ++++"
           slackSend channel: 'devops', message: "$JOB_NAME HAS BEEN FAILED"             
         }
       }
     }
   }
}
