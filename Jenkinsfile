pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git(url: 'https://github.com/ronakfinaviya/pipe_test.git', poll: true, branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sh '''python --version
cd /Users/ronakfinavia/PycharmProjects/pipe_test
'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test1') {
          steps {
            sh 'python test1.py'
          }
        }

        stage('Test2') {
          steps {
            sh 'Python test2.py'
          }
        }

        stage('Test3') {
          steps {
            sh 'python test3.py'
          }
        }

        stage('Test4') {
          steps {
            sh 'python test4.py'
          }
        }

      }
    }

    stage('End') {
      steps {
        echo 'Finished'
      }
    }

  }
}