pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Правильный синтаксис для checkout из Git
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    extensions: [],
                    userRemoteConfigs: [[
                        url: 'https://github.com/ignatuschka/test-jenkins-repo.git'
                    ]]
                ])
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building on macOS: $(uname -a)"'
            }
        }
    }
}
