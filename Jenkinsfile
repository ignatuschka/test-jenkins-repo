pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo "Клонируем репозиторий..."
                git url: 'https://github.com/ignatuschka/test-jenkins-repo.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'echo "Сборка на: $(uname -a)"'
                    sh 'ls -la'
                }
            }
        }
    }
}
