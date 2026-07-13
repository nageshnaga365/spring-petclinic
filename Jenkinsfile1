pipeline {

    agent any

    tools {
        jdk 'JDK21'
        maven 'Maven'
    }

    environment {
        APP_NAME = "spring-petclinic"
    }

    stages {

        stage('Checkout') {
            steps {
                echo "==============================="
                echo "Checking out source code..."
                echo "==============================="

                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "==============================="
                echo "Compiling Project..."
                echo "==============================="

                sh 'mvn clean compile'
            }
        }

        stage('Unit Test') {
            steps {
                echo "==============================="
                echo "Running Unit Tests..."
                echo "==============================="

                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo "==============================="
                echo "Packaging Application..."
                echo "==============================="

                sh 'mvn package'
            }
        }
    }

    post {

        always {
            echo "Pipeline execution completed."
        }

        success {
            echo "Build Successful"
        }

        failure {
            echo "Build Failed"
        }
    }
}
