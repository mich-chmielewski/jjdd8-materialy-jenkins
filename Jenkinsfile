pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Testing') {
      steps {
        sh 'mvn clean'
        sh 'mvn --project biojava-alignment test'
      }
    }

  }
}