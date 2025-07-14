pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git(
                    url: 'https://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@github.com/ignatuschka/test-jenkins-repo.git',
                    branch: 'main'
                )
            }
        }
        stage('Build') {
            steps {
                script {
                    def uname = sh(script: 'uname -a', returnStdout: true).trim()
                    echo "Сборка на: ${uname}"
                    sh 'ls -la'
                }
            }
        }
    }
}
