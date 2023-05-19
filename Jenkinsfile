pipeline {
    agent any
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!'
            }
        }
        stage('Git clone') {
            steps {
                echo 'cloning git repo'
                git branch: 'main', credentialsId: 'git-ssh-key', url: 'git@github.com:zdravko-yanev/jenkins-private.git'
            }
        }



    }
}
