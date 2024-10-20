pipeline {
    agent any
    stages {
        stage('Initialize Terraform') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Plan Terraform') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Apply Terraform') {
            steps {
                sh 'terraform apply -auto-approve'
                sh 'ls -al'  
                sh 'echo $(pwd)/file1.txt'
            }
        }
    }
}
