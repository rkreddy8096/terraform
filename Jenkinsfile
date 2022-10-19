pipeline {
    agent {label 'linux'}
    stages {
        stage('clone') {
           steps{
                git branch: 'master', url: 'https://github.com/futurice/terraform-examples.git'
            }
        }
        stage('checkout'){
            steps{
                checkout scm
            }
        }
        stage('terraform') {
            steps{
                sh 'cd ~'
                sh 'terraform init'
                sh 'terraform apply -auto-approve'
            }
        }
    } 
}
