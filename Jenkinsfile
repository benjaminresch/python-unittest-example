pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh '''find / -type f -name \'nosetests*\' -perm +111 -print -quit

pip install -r requirements.txt

nosetest tests
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