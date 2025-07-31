pipeline {
    agent any

    triggers {
        githubPush() // Triggered by GitHub Webhook
    }
h
    environment {
        PROJECT_NAME = 'my-simple-project'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git credentialsId: 'your-github-credentials-id', url: 'https://github.com/your-org/your-repo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo "Building ${env.PROJECT_NAME}"
                // Example: run a build tool
                sh 'echo Simulating Build...'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example: run test script
                sh 'echo Simulating Tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Example: deploy command
                sh 'echo Simulating Deploy...'
            }
        }
    }
}
