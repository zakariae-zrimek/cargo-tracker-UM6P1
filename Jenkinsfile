pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'develop', url: 'https://github.com/zakariae-zrimek/cargo-tracker.git'
            }
        }

        stage('Build & Test') {
            steps {
                sh 'mvn clean verify'
            }
        }
    }

    post {
        success {
            echo 'Build et tests terminés avec succès ✅'
        }
        failure {
            echo 'Échec du build ou des tests ❌'
        }
    }
}
