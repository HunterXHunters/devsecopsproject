pipeline {
    agent none
    stages {
        stage('GitGuardian Scan') {
            agent {
                docker { image 'gitguardian/ggshield:latest' }
            }
            environment {
                GITGUARDIAN_API_KEY = 'CEad1bD9abbAAdbceEf514a31b6A9c40f0c4D589CC8E3e8Ca7D687bbA7B22f8E7c93cc0'
            }
            steps {
                sh 'ggshield scan ci'
            }
        }
    }
}
