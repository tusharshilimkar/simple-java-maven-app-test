pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'sh \'mvn -B -DskipTests clean package\''
      }
    }

  }
}