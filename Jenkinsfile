pipeline {

    agent  none

    stages {

        stage('Fix the permission issue') {
            agent any 
            steps {
                sh 'sudo docker pull 6-alpine'
            }

        }

        stage ('step 1'){
            agent {
                
                docker {
                    image 'node:6-alpine' 
                    args '-p 3000:3000' 
                }
            }
        }   
        stages {
            stage('Build') { 
                steps {
                    sh 'npm install' 
                }
            }
        }
    }
    
}