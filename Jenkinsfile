pipeline {
  agent any

  stages {
    echo 'Started'

    stage('checkout') {
        git 'https://github.com/ChristopherGerlier/jenkins2-course-spring-boot.git'
    }

    stage ('Compile stage') {
      steps {
        sh 'echo coucou'
        withMaven(maven: 'maven3') {
          sh 'mvn -f spring-boot-samples/spring-boot-samples-atmosphere/pom.xml clean compile'
        }
      }
    }
  }
}