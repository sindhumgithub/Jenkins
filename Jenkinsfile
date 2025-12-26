pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo "I am Building..."
            }
            stages('Test') {
                steps{
                    echo "I am testing..."
                }
            }
            stages('Deploy') {
                steps {
                    echo "I am deploying..."
                }
                
            }
        }
    }
}