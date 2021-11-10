pipeline{
    agent any
   
  stages {
    stage('Install Packages') {
      steps {
        sh 'yarn install'
      }
    }
    stage('Test and Build') {
      parallel {
        stage('Run Tests') {
          steps {
            sh 'yarn test'
          }
        }
        stage('Create Build Artifacts') {
          steps {
            sh 'yarn build'
          }
        }
      }
    }


}
