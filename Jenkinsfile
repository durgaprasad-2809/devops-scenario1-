pipeline {
    agent any

    tools {
        gradle 'gradle'  // This must match the name you configured in Jenkins Global Tools
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'feature/login', url: 'https://github.com/TedlaHaneesh/devops-scenario1.git'
            }
        }

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

        stage('Run Python Script') {
            steps {
                sh 'python3 login.py'
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

