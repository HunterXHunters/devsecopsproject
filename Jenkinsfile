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
    stage ('Source Composition Analysis') {
      steps {
         sh 'rm owasp* || true'
         sh 'wget "https://raw.githubusercontent.com/HunterXHunters/devsecopsproject/main/owasp-dependency-check.sh?token=GHSAT0AAAAAABQ2NE2GZK3UH6TS5WTZ53GAYPSGZ3Q"'
         sh 'chmod +x owasp-dependency-check.sh'
         sh 'bash owasp-dependency-check.sh'
         sh 'cat /var/lib/jenkins/OWASP-Dependency-Check/reports/dependency-check-report.xml'
        
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
