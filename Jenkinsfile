pipeline {
  agent any

  stages {
    stage('checkout') {
      sh 'echo coucou 1'
    }

    stage ('Compile stage') {
      steps {
        sh 'echo coucou 2'
        // withMaven(maven: 'maven3') {
        //   sh 'mvn -f spring-boot-samples/spring-boot-samples-atmosphere/pom.xml clean compile'
        // }
      }
    }
  }
}