pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/krishna7362/javawebmaven.git', branch: 'master')
      }
    }
    stage('build') {
      parallel {
        stage('build') {
          steps {
            bat 'mvn clean install'
          }
        }
        stage('Junit ') {
          steps {
            bat 'mvn test'
          }
        }
      }
    }
  }
}