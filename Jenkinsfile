pipeline {
        agent any

tools {
        jdk 'jdk21'
        maven 'maven'
}

stages {
        stage('checkout'){
        steps {
                checkout scm
}
}
stage('Build') {
        steps {
        sh 'mvn clean package'
        }
      }
    }
}

