pipeline {
    agent {
        label 'linux'
    }
    stages{
        stage('Install molecule') {
            steps{
                sh 'pip3 install -r test-requirements.txt'
            }
        }
        stage('Run molecule'){
            steps{
                sh 'molecule test'
            }
        }
    }

}