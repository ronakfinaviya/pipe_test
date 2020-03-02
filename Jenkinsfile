pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git(url: 'https://github.com/ronakfinaviya/pipe_test.git', poll: true)
      }
    }

    stage('Build') {
      steps {
        sh '''python --version
cd /Users/ronakfinavia/PycharmProjects/pipe_test
'''
      }
    }

  }
}