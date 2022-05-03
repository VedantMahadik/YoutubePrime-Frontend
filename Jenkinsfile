pipeline {
    agent none
    stages {
        stage('Frontend') {
            /*agent {
                docker { 
                    label 'windows'
                    image 'node:lts-alpine' 
                }
            }*/
            steps {
                sh 'node --version'
                sh 'npm install'
                sh 'npm run dev'
            }
        }
    }
}
