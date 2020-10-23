pipeline {
  agent {
    node {
        label 'master'
        customWorkspace '/var/lib/jenkins/'
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
