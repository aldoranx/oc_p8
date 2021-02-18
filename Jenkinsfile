pipeline {
    agent {
         dockerfile {
            filename 'Dockerfile.test'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'sudo composer update --ignore-platform-reqs'
                sh 'sudo composer install --ignore-platform-reqs'
            }
        }
    }
}
