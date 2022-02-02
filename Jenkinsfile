pipeline {
    agent none
    stages {
        stage('GitGuardian Scan') {
            agent {
                docker { image 'gitguardian/ggshield:latest' }
            }
            
            steps {
                sh 'ggshield scan ci'
            }
        }
    }
}
