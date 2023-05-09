pipeline {
  agent any 
  parameters{
    string(name: 'Target_env', description: 'Target environment')
//     choice(name: 'Target_env',choices:['test','prod'],description:'where to deploy')
  }
  environment{
    DEPLOY_TO = "$Target_env"
  }
  stages{
    stage('TEST'){
      when{
        environment name:'DEPLOY_TO', value='test'
      }
      steps{
        sh '''
          sleep 5
          echo "Deploying to test environment"
         '''
      }
    }
    stage('PROD'){
      when{
        environment name:'DEPLOY_TO', value='prod'
      }
      steps{
        sh '''
          sleep 5
          echo "Deploying to prod environment"
         '''
      }
    }
  }
}
    
//   stages {
//     stage('BUILD'){
//       steps{
//         sh '''
//           pwd
//           echo "This is the first stage: BUILD"
//         '''
//       }
//     }
//     stage('TEST'){
//       parallel{
//         stage('TEST1'){
//           steps{
//             sh '''
//             pwd
//             echo "This is the second stage: TEST1"
//           '''
//           }
//         }
//         stage('TEST2'){
//           steps{
//             sh '''
//             pwd
//             echo "This is the second stage: TEST2"
//           '''
//           }
//         }
//       }
//     }
//     stage('DEPLOY'){
//       steps{
//         sh '''
//           pwd
//           echo "This is the third stage: DEPLOY"
//         '''
//       }
//     }
//   }
// }
