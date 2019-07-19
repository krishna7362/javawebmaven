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
  }
}