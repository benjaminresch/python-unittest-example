pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh '''
nosetests tests
tree'''
      }
    }

    stage('clean') {
      steps {
        cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenSuccess: true, cleanWhenUnstable: true, deleteDirs: true)
      }
    }

  }
}