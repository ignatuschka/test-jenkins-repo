pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo "Клонируем репозиторий..."
                git 'https://github.com/ignatuschka/test-jenkins-repo.git'
            }
        }
        stage('Build') {
            steps {
                echo "Сборка на macOS: $(uname -a)"
                sh 'ls -la'  # Проверим содержимое репозитория
            }
        }
    }
}
