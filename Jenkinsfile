pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo composer update --ignore-platform-reqs'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
