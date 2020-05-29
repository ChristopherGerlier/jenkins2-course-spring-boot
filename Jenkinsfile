pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/ChristopherGerlier/jenkins2-course-spring-boot.git'
      }
    }

    stage ('Compiling, test, packaging stage') {
      steps {
        dir('spring-boot-samples/spring-boot-sample-atmosphere') {
          sh 'mvn clean package'
        }
      }
    }

    stage('archival') {
      steps {
        step([$class: 'JUnitResultArchiver', testResults: 'target/surefire-reports/TEST-*.xml'])
        archiveArtifacts 'spring-boot-samples/spring-boot-sample-atmosphere/target/*.jar'
      }
    }
  }
}