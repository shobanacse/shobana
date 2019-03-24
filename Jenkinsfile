pipeline {
    agent any

    stages {
         
        stage('Build') {
          
            
            steps {
                
               
                bat 'start' 
               archiveArtifacts allowEmptyArchive: true, artifacts: '**', fingerprint: true, onlyIfSuccessful: true
            }
        }
    }
}
