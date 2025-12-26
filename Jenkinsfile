// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 echo "I am Building..."
//             }
//         }

//         stage('Test') {
//             steps {
//                 echo "I am testing..."
//             }
//         }

//         stage('Deploy') {
//             steps {
//                 echo "I am deploying..."
//             }
//         }
//     }
// }


pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "I am building agent-1 node"
            }
        }
        stage('Test') {
            steps {
                echo "I am testing agent-1 node"
            }
        }
        stage('Deploy') {
            steps {
                echo "I am deploying agent-1 node"
            }
        }
    }
}
