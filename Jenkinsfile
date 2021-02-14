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
      post {
        success {
          junit '**/target/surefire-reports/TEST-*.xml' 
        }
      }
    }
    stage ('Build Docker image') {
      sh "whoami"
      sh "ls -all /var/run/docker.sock"
      sh "mv ./target/hello*.jar ./data" 
      
      dockerImage = docker.build("hello-world-java")
    }
  }
}