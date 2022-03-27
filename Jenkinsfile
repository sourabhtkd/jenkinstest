pipeline {
        agent any
  stages {
  
    stage('ONE'){
      steps {
        echo 'Hwllo first stage'
      }
    }
    
    stage('Two'){
      steps {
        input('Do  you want to proceed')
      }
    }
    
    stage('Three'){
      when {
        not { 
          branch "master"
        }
      }
      steps {
        echo "three"
      }
    }
  }

}
