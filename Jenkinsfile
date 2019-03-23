pipeline {
    agent any

    stages {

        // Normal Stages

        stage('build') {
            steps {
                bat "start"
            }
        }
    }

    post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }

        always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "padmini.ramachandra@mindtree.com",
                sendToIndividuals: true])
        }
    }
}
