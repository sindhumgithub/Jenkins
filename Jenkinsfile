pipeline {
    stages {
        stage('Build'){
            steps{
                echo "Building..."

            }
        }
    }
    stages('Test'){
        steps{
            echo "Testing..."
        }   
    }
    stages('Deploy'){
            steps{
                echo "Deploying..."
        }
    }
post {
    always {
        echo "I am always saying hello again"
        cleanWS()
    }
    success {
        echo "I will run if  I am sucess"
    }
    failure {
        echo "I will run If I am failure"
    }
}
}
