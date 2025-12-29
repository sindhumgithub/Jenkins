pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        env
                    """
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
            }
        }
    }

    post {
        always {
            echo 'Cleaning workspace'
            cleanWs()
        }
        success {
            echo 'Build successful'
        }
        failure {
            echo 'Build failed'
        }
    }
}
