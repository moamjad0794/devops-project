pipeline {
    agent {
        node 'maven'
    }
    
    environment {
        PATH = "/usr/bin:$PATH"
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment Phase'
                    // You can add deployment commands here.
                }
            }
        }
    }

    post {
        success {
            echo 'Build and test successful!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
