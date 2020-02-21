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
        stage('delete none tag images') {
            steps {
                sh 'docker images | grep none | awk '{ print $3; }' | xargs docker rmi'
            }
        }
    }
}
