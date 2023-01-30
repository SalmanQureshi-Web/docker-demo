pipeline {
    agent any
    stages {
        stage('Initialize') {
            steps {
                echo 'Initializing...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy to Docker') {
            steps {
                echo 'Deploying to Docker...'
                sh 'docker build -t hello-world:0.1 .'
                sh 'docker run --detach --publish 8091:3000 hello-world:0.1'
            }
        }
    }

}
