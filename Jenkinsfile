pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/ignatuschka/test-jenkins-repo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building on macOS: $(uname -a)"'
            }
        }
    }
}
