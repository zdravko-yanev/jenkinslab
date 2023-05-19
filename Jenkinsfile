pipeline {
    agent kubernetes
    stages {
        stage('Git clone') {
            steps {
                echo 'cloning git repo'
                git branch: 'main', credentialsId: 'git-repo-token', url: 'https://github.com/zdravko-yanev/jenkins-private.git'
            }
        }

    stage('Docker Build') {
      steps {
      	sh 'docker build -t myimage:latest .'
      }
    }

    }
}
