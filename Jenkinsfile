node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("prestashop/prestashop-git")
    }

    stage('Run image') {
        docker.image('prestashop/prestashop-git').withRun('-p 8065:80') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }

    }
    
}
