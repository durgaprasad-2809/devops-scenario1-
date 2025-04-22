pipeline {
    agent any

    tools {
        gradle 'gradle'  // This must match the name you configured in Jenkins Global Tools
    }

    stages {
        stage('Build') {
            steps {
                sh 'gradle clean build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
    }
}
