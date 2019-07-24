pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/krishna7362/javawebmaven.git'
      }
    }
    stage('compile') {
      steps {
        bat 'mvn compile'
      }
    }
    stage('junit test') {
      steps {
        bat 'mvn test'
      }
    }
    stage('SonarQube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
    stage('deploy') {
      steps {
        bat 'REM'
      }
    }
  }
}