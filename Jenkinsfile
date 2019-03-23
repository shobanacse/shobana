pipeline {  
     agent any  
     stages {  
         stage('Build') {  
             steps {  
                 bat "start" 
             }  
         }  
     }  
    post {
    failure {
        mail to: 'padmini.ramachandra@mindtree.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
    }
}
 }
