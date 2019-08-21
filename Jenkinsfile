pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    git 'https://github.com/vegirajukanishka/kubernetesfiles.git'
                    sh label: '',script: 'sudo kubectl apply -f rc.yml'
                    sh label: '',script: 'sudo kubectl get rc'
                    sh label: '',script: 'sudo kubectl apply -f service.yml'
                    sh label: '',script: 'sudo kubectl get svc'
                }
            }
        }
        }
}
