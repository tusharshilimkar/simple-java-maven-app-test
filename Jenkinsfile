pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
        echo 'Testing Done'
      }
    }

    stage('deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
      }
    }

    stage('end') {
      steps {
        echo 'ALL OK'
      }
    }

  }
}
