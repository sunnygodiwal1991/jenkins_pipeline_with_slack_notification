pipeline {  
   agent any
   stages {         
     stage('Install Dependencies') { 
       steps {
         // slackSend channel: 'devops', message: 'Job Started' 
         slackSend channel: 'devops', message: "$JOB_NAME Job Started"
         sh 'echo "Install Dependencies..."' 
       }
     }
     
     stage('Test') { 
       steps {
         // slackSend channel: 'devops', message: 'Testing' 
         slackSend channel: 'devops', message: "$JOB_NAME Testing"            
         sh 'echo "testing application..."'
       }
     }

     stage("Deploy application") { 
       steps {
         // slackSend channel: 'devops', message: 'Deploying' 
         slackSend channel: 'devops', message: "$JOB_NAME Deploying"            
         sh 'echo "deploying application..."'
       }
     }
   }
}
