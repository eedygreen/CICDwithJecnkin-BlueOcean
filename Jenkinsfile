pipeline {

    agent { none }

    stages {

        stage('Fix the permission issue') {
            agen { any }
            steps {
                sh 'sudo chown root:jenkins /var/run/docker.sock'
            }

        }

        stage('Step 1') {

            agent { docker { iamge 'node:6-alpine'} }
                steps {
                        args '-p 3000:3000'
                    }
                }   

        stage('Build') {

            steps {

                sh 'npm install'
            }

        }   
    }
}
