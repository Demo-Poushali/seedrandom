
pipeline {
    agent any   // Runs on any available agent/worker node

    triggers {
        githubPush()  // ✅ Trigger build when GitHub webhook fires (on push)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm   // Pulls your repo code
            }
        }

        stage('Build') {
            steps {
                echo "Running build steps..."
                // Example: sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example: sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Example: sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo "✅ Build succeeded!"
        }
        failure {
            echo "❌ Build failed!"
        }
    }
}

