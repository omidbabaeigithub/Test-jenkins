pipeline {
  agent any
  stages {
    stage('First') {
      parallel {
        stage('First') {
          steps {
            sh 'echo \'First Step\''
            echo 'Hi'
            sleep 10
          }
        }
        stage('Second') {
          steps {
            sh 'ls'
          }
        }
      }
    }
    stage('Third') {
      steps {
        timeout(time: 10, activity: true)
      }
    }
  }
}