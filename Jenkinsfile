pipeline {
        agent any

tools {
        jdk 'JDK21'
        maven 'Maven'
}

stages {
        stage('checkout'){
        steps {
                checkout SCM
}
}
stage('Build') {
        steps {
        sh 'mvn clean package'
        }
      }
    }
}

