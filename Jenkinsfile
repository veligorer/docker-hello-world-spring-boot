pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        script {
          sh 'mvn clean package'
        }
      }
    }
  }
}