pipeline {
    agent { 
         dockerfile {
            filename 'Dockerfile.test'
        }
    }
    stages {
        stage('Pre-Build') {
            steps {
                sh 'composer update --ignore-platform-reqs'
                sh 'composer install --ignore-platform-reqs'
                sh 'sudo php -d date.timezone=UTC ./vendor/bin/phpunit -c tests/Unit/phpunit.xml'
            }
        }
        stage('Build') {
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
