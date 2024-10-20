pipeline {
    agent any
    stages {
        stage('Initialize Terraform') {
            steps {
                sh 'terraform init'
            }
        }
        stage('destroy Terraform') {
            steps {
                sh 'terraform destroy'
    }
}
    }
}
