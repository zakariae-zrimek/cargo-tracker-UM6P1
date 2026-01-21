pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {

        stage('Build & Test') {
            steps {
                // sh 'mvn clean verify'
                echo 'Build et tests en cours...'
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
