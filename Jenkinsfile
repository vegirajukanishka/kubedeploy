pipeline {
    agent any 
    stages {
        stage ('deployment') {
            steps {
                node ('kubemaster') {
                    sh label:'',script: 'sudo docker login --username kanishkaraju --password kanishka@13'
                    sh label: '',script: 'sudo docker pull kanishkaraju/raju:gol.5'
                    sh label: '',script: 'sudo kubectl apply -f rc.yml'
                    sh label: '',script: 'sudo kubectl apply -f service.yml'
                }
            }
        }
        }
}
