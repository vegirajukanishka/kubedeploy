pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    sh label: '',script: 'sudo kubectl apply -f rc.yml.'
                    sh label: '',script: 'sudo kubectl apply -f service.yml.'
                }
            }
        }
        }
}
