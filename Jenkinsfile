pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        sh 'echo List files'
        sh 'ls -ls'
        sh 'checkout project'
        sh 'pwd'
        git 'https://github.com/ChristopherGerlier/jenkins2-course-spring-boot.git'
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