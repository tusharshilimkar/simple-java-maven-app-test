pipeline {
  agent any
  stages {
    stage('build') {
      steps {
#        sh 'mvn -B -DskipTests clean package'
         sh 'echo $PATH'       
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
