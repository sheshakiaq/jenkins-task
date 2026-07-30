pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        git url: 'https://github.com/sheshakiaq/jenkins-task.git', branch:'main'
      }
    }
    
    stage('Build'){
      steps{
        echo "Building Started..."
      }
    }
    
    stage('Test'){
      steps{
        echo "Testing Happening..."
      }
    }
    
    stage('Deployment'){
      steps{
        echo "Deployment process initiated"
      }
    }
  }
  
  post{
    always{
      archiveArtifacts artifacts:'index.html',
      fingerprint:true
    }
    success{
      echo 'Build Done'
    }
    failure{
      echo 'Build failed'
    }
  }
}
