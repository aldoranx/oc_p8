pipeline {
    agent { 
         docker {
            filename 'Dockerfile.test'
        }
    }
    stages {
        stage('install') {
            steps {
                sh 'sudo composer update --ignore-platform-reqs'
                sh 'sudo composer install --ignore-platform-reqs'
            }
        }
        stage('unitTest') {
            steps {
                sh 'sudo php -d date.timezone=UTC ./vendor/bin/phpunit -c tests/Unit/phpunit.xml'
            }
        }
        
    }
    post {
        always {
            archiveArtifacts artifacts: 'vendor/', fingerprint: true
        }
    }
}
