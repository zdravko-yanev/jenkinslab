pipeline {
    agent any
    stages {
        stage('Git clone') {
            steps {
                echo 'cloning git repo'
                git branch: 'main', credentialsId: 'git-ssh-key', url: 'git@github.com:zdravko-yanev/jenkins-private.git'
            }
        }

    stage('Docker Build') {
      steps {
      	sh 'docker build -t myimage:latest .'
      }
    }

    }
}
