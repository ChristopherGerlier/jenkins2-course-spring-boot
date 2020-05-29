pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/ChristopherGerlier/jenkins2-course-spring-boot.git'
      }
    }

    stage ('Compile stage') {
      steps {
        dir('spring-boot-samples/spring-boot-sample-atmosphere') {
          sh 'mvn clean package'
        }
        archiveArtifacts 'spring-boot-samples/spring-boot-sample-atmosphere/target/*.jar'
      }
    }
  }
}