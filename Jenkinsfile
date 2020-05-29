pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        sh 'echo List files'
        sh 'ls -ls'
        sh 'echo where are we'
        sh 'pwd'
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