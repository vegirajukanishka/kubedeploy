pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    git 'https://github.com/vegirajukanishka/kubernetesfiles.git'
                    sh label: '',script: '''cp -i /etc/kubernetes/admin.conf $HOME/'''
                    sh label: '',script: '''kubectl apply -f rc.yml'''
                    sh label: '',script: '''kubectl apply -f service.yml'''
                }
            }
        }
        }
}
