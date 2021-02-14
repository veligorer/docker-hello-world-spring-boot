pipeline {
  agent any
  tools {
    maven 'Maven 3.6.3'
  }
  stages {
    stage('Build Project') {
      steps {
        script {
          sh 'mvn -Dmaven.test.failure.ignore clean package'
        }
      }
    }
  }
}