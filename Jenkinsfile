pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    git 'https://github.com/vegirajukanishka/kubernetesfiles.git'
                    sh label: '',script: '''sudo cp -i /etc/kubernetes/admin.conf $HOME/'''
                    sh label: '',script: '''sudo kubectl apply -f rc.yml'''
                    sh label: '',script: '''sudo kubectl apply -f service.yml'''
                }
            }
        }
        }
}
