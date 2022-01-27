pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    // Stage 1: Build
    stage ('Build') {
      steps {
          sh 'mvn clean package'
       }
    }
    
    // Stage 2: Testing
    
    stage ('Testing'){
        steps{
            echo 'testing'
        }
    }
    
    // Stage 3: SCA
    
    stage ('SCA'){
        steps{
            echo 'SCA'
            sh "bash script.sh"
            echo "worked"
        }
    }

    // Stage 3: Deploying
    stage ('Deploy') {
      steps {
          echo 'deployed in the Nexus'
       }
    }


    
  }
}
