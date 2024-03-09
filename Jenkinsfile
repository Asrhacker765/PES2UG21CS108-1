pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS108-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                // Your deploy steps go here
                echo 'Deploy'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
}
