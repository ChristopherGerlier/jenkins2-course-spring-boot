pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        sh 'echo checkout project'
        git 'https://github.com/ChristopherGerlier/jenkins2-course-spring-boot.git'
      }
    }

    stage ('Compile stage') {
      steps {
        sh 'echo coucou 2'
        sh 'mvn -f spring-boot-samples/spring-boot-sample-atmosphere/pom.xml clean package'
      }
    }
  }
}