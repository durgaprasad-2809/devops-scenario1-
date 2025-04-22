pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/TedlaHaneesh/devops-scenario1.git'
            }
        }

        stage('Build') {
            steps {
                // Run Gradle build using the system-installed Gradle
                sh 'gradle clean build'
            }
        }

        stage('Test') {
            steps {
                // Here you can add your testing commands if needed
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                // Here you can add your deployment commands if needed
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            // This will always run after the pipeline, for cleanup or final actions
            echo 'Cleaning up...'
        }
    }
}

