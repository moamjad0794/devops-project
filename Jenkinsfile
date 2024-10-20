pipeline {
    agent {
        node 'maven'
    }

    tools {
        maven 'Maven3'  // Ensure Maven is installed on Jenkins and configured
        jdk 'JDK11'     // Ensure JDK is installed and configured in Jenkins
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
