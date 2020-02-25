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
                sh 'docker build -t bhuvnesh94/springboot_hello:latest .'
            }
        }
         stage('docker image run') {
            steps {
                sh 'docker-compose up -d'
            }
        }
         stage('None tag docker image delete') {
            steps {
                sh 'docker images | grep "none" | awk '{print $3}''
            }
        }
    }
}
