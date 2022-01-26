pipeline{
    //Directives
    agent any
    tools {
        maven 'Maven'
    }

    stage {
        //stage 1. Build
        stage ('Build'){
            steps {
                sh 'mvn clean packagae'
            }
        }

        // Stage 2: Testing
        stage ('Test'){
            steps{
                echo 'testing.......'
            }
        }

        // Stage 3: Deploying

        stage ('Deploy'){
            steps{
                echo 'deploying.....'
            }
        }
    }
}

