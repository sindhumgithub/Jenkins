pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo "I am Building..."
            }
            steps('Test') {
                echo "I am testing..."
            }
            steps('Deploy') {
                echo "I am deploying..."
            }
        }
    }
}