pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ -o  PES1UG20CS208 new.cpp'
        build job: 'PES1UG20CS208-1'
      }
    }
    stage('Test'){
      steps{
        sh './PES1UG20CS208'
      }
    }
   stage('Deploy'){
      steps{
        echo 'Deploying'
        sh "exit 1"

      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
