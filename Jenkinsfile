pipeline {
    agent any

    stages {
        stage('Create an image') {
            steps {
                sh 'docker build . -t hello-app'
            }
        }
        stage('Create a container') {
            steps {
                sh 'docker run -p 4002:3000 --name test -d hello-app'
            }
        }
    }
}
