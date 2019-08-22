pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    git 'https://github.com/vegirajukanishka/kubernetesfiles.git'
                    sh label: '',script: '''sudo kubectl apply -f /home/jenkins/workspace/kubedeploy@2/rc.yml'''
                    sh label: '',script: '''sudo kubectl apply -f /home/jenkins/workspace/kubedeploy@2/service.yml'''
                }
            }
        }
        }
}
