pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo "Клонируем репозиторий через SSH..."
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    extensions: [],
                    userRemoteConfigs: [[
                        url: 'git@github.com:ignatuschka/test-jenkins-repo.git',
                        credentialsId: 'e825c3d9-841c-49ff-bea4-b164687ecca9'
                    ]]
                ])
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
