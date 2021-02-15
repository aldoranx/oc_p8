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
                sh 'composer install --ignore-platform-reqs'
            }
        }
    }
}
