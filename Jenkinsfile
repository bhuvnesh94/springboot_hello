pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'sudo mvn install'
            }
        }
        stage('docker image build') {
            steps {
                sh 'docker build -t bhuvnesh94/springboot_hello:latest .'
            }
        }
         stage('docker image run') {
            steps {
                sh 'docker rm -f hello-world'
                sh 'docker-compose up -d'
            }
        }
    }
}
