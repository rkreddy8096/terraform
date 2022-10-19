pipeline {
    agent {label 'linux'}
    stages {
        stage('clone') {
           steps{
                git branch: 'master', url: 'https://github.com/futurice/terraform-examples.git'
            }
        }
        stage('terraform') {
            steps{
                sh 'cd /temp'
                sh 'terraform init'
                sh 'terraform apply -auto-approve'
            }
        }
    } 
}
