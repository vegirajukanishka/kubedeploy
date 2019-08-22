pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    git 'https://github.com/vegirajukanishka/kubernetesfiles.git'
                    sh label: '',script: '''kubectl apply -f rc.yml'''
                    sh label: '',script: '''kubectl apply -f service.yml'''
                }
            }
        }
        }
}
