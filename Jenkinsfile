pipeline {
    agent any
    
    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders:'padmini.ramachandra@mindtree.com', subject: 'Test'
        }
    }
}
