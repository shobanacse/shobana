pipeline {  
     agent any  
     stages {  
         stage('Test') {  
             steps {  
                 sh 'echo "Fail!"; exit 1'  
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
