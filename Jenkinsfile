pipeline {
  agent any 
  stages {
    stage('BUILD'){
      steps{
        sh '''
          pwd
          echo "This is the first stage: BUILD"
        '''
      }
    }
    stage('TEST'){
      parallel{
        stage('TEST1'){
          steps{
            sh '''
            pwd
            echo "This is the second stage: TEST1"
          '''
          }
        }
        stage('TEST2'){
          steps{
            sh '''
            pwd
            echo "This is the second stage: TEST2"
          '''
          }
        }
      }
    }
    stage('DEPLOY'){
      steps{
        sh '''
          pwd
          echo "This is the third stage: DEPLOY"
        '''
      }
    }
  }
}
