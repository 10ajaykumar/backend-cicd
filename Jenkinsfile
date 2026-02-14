pipeline {
    agent any

    stages {

        stage('Terraform Init') {
            steps {
                dir('simple-test') {
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform Plan') {
            steps {
                dir('simple-test') {
                    sh 'terraform plan'
                }
            }
        }

        stage('Terraform Apply') {
            steps {
                dir('simple-test') {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
