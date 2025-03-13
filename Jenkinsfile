pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS591-1'
                sh 'g++ -o hello_exec hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment step...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
