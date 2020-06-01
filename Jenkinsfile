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
          sh 'mvn clean verify'
        }
      }
    }

    stage('archival') {
      steps {
        publishHTML([allowMissing: true, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'spring-boot-samples/spring-boot-sample-atmosphere/target/site/jacoco', reportFiles: 'index.html', reportName: 'Code Coverage', reportTitles: ''])
        step([$class: 'JUnitResultArchiver', testResults: 'spring-boot-samples/spring-boot-sample-atmosphere/target/surefire-reports/TEST-*.xml'])
        archiveArtifacts 'spring-boot-samples/spring-boot-sample-atmosphere/target/*.jar'
      }
    }
  }
}