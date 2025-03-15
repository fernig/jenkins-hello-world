pipeline {
  agent any
  stages {
    stage('Echo Version') {
      steps {
        sh '''echo "Show version"
mvn version'''
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package -DskipTest=true'
      }
    }

    stage('Unit Test') {
      steps {
        script {
          for (int i=0; i<60; i++) {
            echo "${i+1}"
            sleep 1
          }
          sh "mvn test"
        }

      }
    }

  }
}