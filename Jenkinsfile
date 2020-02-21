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
         stage('docker image build') {
            steps {
                sh 'docker run -d --name=hello-world -p 8081:8080 bhuvnesh94/springboot_hello:latest'
            }
        }
    }
}
