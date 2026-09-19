```groovy
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Repository checkout successful!'
            }
        }

        stage('System Information') {
            steps {
                sh 'echo "===== SYSTEM INFO ====="'
                sh 'pwd'
                sh 'whoami'
                sh 'java -version'
                sh 'git --version'
            }
        }

        stage('Build') {
            steps {
                echo '===== BUILD STAGE ====='
                sh 'echo "Build started..."'
                sh 'echo "Build completed successfully!"'
            }
        }

        stage('Test') {
            steps {
                echo '===== TEST STAGE ====='
                sh 'echo "Running tests..."'
                sh 'echo "All tests passed!"'
            }
        }

        stage('Complete') {
            steps {
                echo '===== PIPELINE COMPLETE ====='
                echo 'Jenkins Pipeline executed successfully!'
            }
        }
    }

    post {
        success {
            echo '✅ BUILD SUCCESSFUL'
        }

        failure {
            echo '❌ BUILD FAILED'
        }

        always {
            echo 'Pipeline execution finished.'
        }
    }
}
```
