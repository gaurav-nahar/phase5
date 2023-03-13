pipeline {

    agent any

    stages {
        stage('Checkout') {
            steps {
                 checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'c8430932-7b9c-4fa6-8799-bce2abbb142f', url: 'https://github.com/deepanshu999/EmployeeManagementSystem.git']])
            }
        }
        stage('Build') {
            steps {
                git credentialsId: 'c8430932-7b9c-4fa6-8799-bce2abbb142f', url: 'https://github.com/gaurav-nahar/phase5.git'
                sh 'mvn -B -phase5 clean package' 
                
            }
        }
    }
}