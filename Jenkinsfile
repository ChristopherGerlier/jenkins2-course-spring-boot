pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        sh 'echo List files'
        sh 'ls -ls'
      }
    }

    stage ('Compile stage') {
      steps {
        sh 'echo coucou 2'
        sh 'mvn -f spring-boot-samples/spring-boot-samples-atmosphere/pom.xml clean compile'
      }
    }
  }
}