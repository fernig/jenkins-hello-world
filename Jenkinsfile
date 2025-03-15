pipeline {
  agent any
  stages {
    stage('Echo Version') {
      steps {
        sh '''echo "Show version"
mvn version'''
      }
    }

  }
}