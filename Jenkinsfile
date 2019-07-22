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
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }
    stage('deploy') {
      steps {
        bat 'REM'
      }
    }
  }
}