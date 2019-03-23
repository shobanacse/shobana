pipeline {
    agent any

    stages {

        // Normal Stages

        stage ('Build'){
            bat "run"
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
