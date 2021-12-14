pipeline {  
   agent any
   stages {         
     stage('Install Dependencies') { 
       steps {
         slackSend channel: 'devops', message: 'Job Started' 
         sh 'echo "Install Dependencies..."' 
       }
     }
     
     stage('Test') { 
       steps { 
         sh 'echo "testing application..."'
       }
     }

     stage("Deploy application") { 
       steps { 
         sh 'echo "deploying application..."'
       }
     }
   }
}
