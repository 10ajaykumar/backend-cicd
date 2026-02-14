pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git url: 'https://github.com/10ajaykumar/backend-cicd.git',
                    branch: 'main'
            }
        }

        stage('Terraform Init') {
            steps {
                dir('backend') {
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform Plan') {
            steps {
                dir('backend') {
                    sh 'terraform plan'
                }
            }
        }

        stage('Terraform Apply') {
            steps {
                dir('backend') {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
