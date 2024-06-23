pipeline {
    agent any
    stages {
        stage('Cloning Git') {
            steps {
                sh "ls -lat"
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook(
                    credentialsId: 'e1f20ff2-45df-447f-b2e9-7745db50a359',
                    inventory: 'dev.inv',
                    playbook: 'copy.yaml'
                )
            }
        }
    }
}
