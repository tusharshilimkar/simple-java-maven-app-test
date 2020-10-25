pipeline {
  agent {label 'master'}
  tools{maven 'Apache-Maven-3.5.4'}
  stages {
    stage('build') {
      steps {
         sh 'echo $USER'  
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
