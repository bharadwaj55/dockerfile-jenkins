
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git branch: 'main', url: 'https://github.com/bharadwaj55/testdocker.git'
                sh 'pwd; ls -ltr'
            }
        }
        stage('DockerBuild') {
            steps {
                sh """
                cat Dockerfile
                docker build -t deployimage:latest .
                """
            }
        }
    }
}

