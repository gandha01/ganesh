pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/gandha01/ganesh.git', branch: 'master')
      }
    }
    stage('testing') {
      parallel {
        stage('testing') {
          steps {
            sh 'echo \'runing is unit test\''
          }
        }
        stage('functional_test') {
          steps {
            sh 'echo \'functional test\''
          }
        }
      }
    }
    stage('deploy to QA') {
      steps {
        sh 'echo \'deploy to QA\''
      }
    }
    stage('system testing') {
      steps {
        sh 'echo \'system testing\''
      }
    }
    stage('deploy to Prod') {
      steps {
        sh 'echo \'deploy to Prod\''
      }
    }
  }
}