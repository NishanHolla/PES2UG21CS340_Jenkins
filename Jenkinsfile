pipeline{
  agent any{
    stages('Build'){
      steps{
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test'){
      steps{
      sh './output'
      }
    }
  }
  stage('Deploy'){
    steps{
      echo 'Deploy'
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
