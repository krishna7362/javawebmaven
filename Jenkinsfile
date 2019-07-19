pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/krishna7362/javawebmaven.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        bat 'mvn clean install'
      }
    }
    stage('SonarQube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
    stage('Test') {
      steps {
        bat 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        bat 'xcopy "C:\\Program Files (x86)\\Jenkins\\workspace\\javawebmaven_master\\target\\javawebmaven.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
      }
    }
  }
}