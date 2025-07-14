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
                    // Вариант 1: Через переменную
                    def uname = sh(script: 'uname -a', returnStdout: true).trim()
                    echo "Сборка на macOS: ${uname}"
                    
                    // Вариант 2: Через отдельную sh-команду
                    sh 'echo "Сборка на macOS: $(uname -a)"'
                    
                    sh 'ls -la'  // Проверим содержимое репозитория
                }
            }
        }
    }
}
