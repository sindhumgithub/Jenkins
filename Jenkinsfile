pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }
    options {
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {  //This is build section
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        env
                        echo "Hello &{params.PERSON}"
                        echo "Biography &{params.BIOGRAPHY}"
                        echo "Deploy &{params.DEPLOY}"
                        echo "Choice &{params.CHOICE}"
                        echo "Password &{params.PASSWORD}"
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
        aborted {
            echo 'Build is Aborted'
        }
    }
}
