pipeline {
    environment {
        //This variable need be tested as string
        doError = '1'
    }

    agent any

    stages {
     
        stage('Error') {
            when {
                expression { doError == '1' }
            }
            steps {
                echo "Failure"
                error "failure test. It's work"
                step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "padmini.ramachandra@mindtree.com",
sendToIndividuals: true])
            }
        }

        stage('Success') {
            when {
                expression { doError == '0' }
            }
            steps {
                echo "Ok"
                echo "ok"
            }
        }
    }
    post {
      always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "padmini.ramachandra@mindtree.com",
                sendToIndividuals: true])
        }
    }
}

