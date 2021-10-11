pipeline {
    agent {
        label 'linux'
    }
    stages{
        stage('Checkout') {
            steps{
                git branch: 'main', credentialsId: '2cca28be-e634-40b5-9eac-f4b1bb42e847', url: 'https://github.com/falconow/kibana-role'
            }
        }
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