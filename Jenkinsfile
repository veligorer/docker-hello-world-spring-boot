def mvnHome
pipeline {
  agent any
  tools {
    maven 'Maven 3.6.3'
  }
  stages {
    stage('build') {
      steps {
        script {
          mvnHome = tool 'maven-3.6.1'
          echo "${mvnHome}"
          sh 'mvn clean package'
          
        }
      }
    }
  }
}