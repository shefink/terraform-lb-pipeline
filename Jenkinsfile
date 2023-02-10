pipeline {
    agent any

    stages {
        stage('clone from github') {
            steps {
                git branch: 'main', url: 'https://github.com/mohammedashiqu/terraform-aws-loadbalancer-project.git'
            }
        }
        stage('terraform initialization') {
            steps {
                terraform init
            }
        }
        stage('terraform applying') {
            steps {
                terraform apply --auto-approve
            }
        }
    }
}
