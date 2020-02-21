pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('docker image build') {
            steps {
                sh 'sudo docker build -t bhuvnesh94/springboot_hello:latest .'
            }
        }
    }
}