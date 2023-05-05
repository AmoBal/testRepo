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
      steps{
        sh '''
          pwd
          echo "This is the first stage: TEST"
        '''
      }
    }
    stage('DEPLOY'){
      steps{
        sh '''
          pwd
          echo "This is the first stage: DEPLOY"
        '''
      }
    }
  }
}
