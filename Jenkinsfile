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
          stage("Four"){
                  parallel {
                          stage('Unit Test'){
                                  steps {
                                    echo "Running Unit test......"
                                  }
                          }
                          stage("Integration Test"){
                                  agent {
                                          docker {
                                           reusenode false
                                           image 'ubuntu'
                                          }
                                  }
                                  steps {
                                   echo "Running integration test ....."
                                  }
                          }
                  }
          }
  }

}
