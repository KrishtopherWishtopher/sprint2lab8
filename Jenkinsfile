pipeline
{
  agent any
  environment 
  {
          IMAGE_NAME = "team-skeleton"
  }
  stages
  {
    stage('Checkout')
    {
      steps
      {
        echo "fail before checkout"
        checkout scm
        echo "fail after checkout"
      }
    }
    stage('Build Image')
    {
      steps
      {
        echo "fail before build"
        sh 'docker build -t team-skeleton:${BUILD_NUMBER} .'
        echo "fail after build"
      }
    }
    stage('Test')
    {
      steps
      {
        sh 'mvn -B test'
      }
    }
  }
}
