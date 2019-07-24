pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/Ajayvarma8142/javawebmaven.git', branch: 'master')
      }
    }
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            bat 'mvn compile'
          }
        }
        stage('junit-test') {
          steps {
            bat 'mvn test'
          }
        }
      }
    }
    stage('SonarQube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
    stage('Deploy') {
      steps {
        bat 'REM'
      }
    }
  }
}