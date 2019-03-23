pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                bat "run"
            }
        }
    }
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders:'padmini.ramachandra@mindtree.com', subject: 'Test'
        }
    }
}
