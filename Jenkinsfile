pipeline {
    agent any
    environment {
        WORK_DIR = "/home/JenkinsPoorvika/Terraformm/"
    }
    stages {
        stage('Initialize Workspace') {
            steps {
                sh 'mkdir -p $WORK_DIR'
                dir("$WORK_DIR") {
                    sh 'cp -r $WORKSPACE/* .'
                }
            }
        }
        stage('Initialize Terraform') {
            steps {
                dir("$WORK_DIR") {
                    sh 'terraform init'
                }
            }
        }
        stage('Apply Terraform') {
            steps {
                dir("$WORK_DIR") {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
