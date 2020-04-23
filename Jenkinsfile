pipeline {

    agent none

    stages {

        stage('Fix the permission issue') {

            agent any

            steps {
                sh 'sudo chown root:jenkins /var/run/docker.sock'
            }

        }

        stage('Step 1') {

            agent {

                docker {
                    steps {
                        image 'node:6-alpine'
                        args '-p 3000:3000'
                    }
                }                
                }
            }
        

        stage('Build') {

            steps {

                sh 'npm install'
            }

        }   
    }
}
