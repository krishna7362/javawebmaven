pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/krishna7362/javawebmaven.git'
      }
    }
    stage('build') {
      steps {
        bat 'mvn clean install'
      }
    }
    stage('junit test') {
      steps {
        bat 'mvn test'
      }
    }
    stage('sonar qube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
    stage('deploy') {
      steps {
        bat 'xcopy "C:\\Program Files (x86)\\Jenkins\\workspace\\mydemo-pipeline_master\\target\\javawebmaven.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
      }
    }
  }
}