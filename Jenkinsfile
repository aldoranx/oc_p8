pipeline {
    agent {
         dockerfile {
            filename 'Dockerfile.test'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'composer update --ignore-platform-reqs'
                h 'composer install --ignore-platform-reqs'
            }
        }
 
