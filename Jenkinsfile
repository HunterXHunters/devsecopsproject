pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    
        // Stage 2: Testing
    
    stage ('Testing'){
        steps{
            snykSecurity failOnIssues: false, organisation: 'sunerarech', projectName: 'devsecops', snykInstallation: 'Please define a Snyk installation in the Jenkins Global Tool Configuration. This task will not run without a Snyk installation.', snykTokenId: 'Snyk-Jenkins', targetFile: 'pom.xml'
        }
    }
    
    
    
    
    // Stage 1: Build
    stage ('Build') {
      steps {
          sh 'mvn clean package'
       }
    }
    
    // Stage 2: Testing
    
    stage ('Testing'){
        steps{
            snykSecurity failOnIssues: false, organisation: 'sunerarech', projectName: 'devsecops', snykInstallation: 'Please define a Snyk installation in the Jenkins Global Tool Configuration. This task will not run without a Snyk installation.', snykTokenId: 'Snyk-Jenkins', targetFile: 'pom.xml'
        }
    }
    


    // Stage 4: Deploying
    stage ('Deploy') {
      steps {
          echo 'deployed in the Nexus'
       }
    }


    
  }
}
