pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'composer update --ignore-platform-reqs'
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
