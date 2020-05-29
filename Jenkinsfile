pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        sh 'echoList files'
        sh 'ls -ls'
      }
    }

    stage ('Compile stage') {
      steps {
        sh 'echo coucou 2'
        withMaven(maven: 'maven3') {
          sh 'mvn -f spring-boot-samples/spring-boot-samples-atmosphere/pom.xml clean compile'
        }
      }
    }
  }
}