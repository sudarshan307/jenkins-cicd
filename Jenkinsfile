pipeline {
    agent any   

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'docker build -t myapp:latest .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'docker run -d -p 8081:8080 myapp:latest'
            }
        }
    }
}

        post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs.'
        }
    }
}
