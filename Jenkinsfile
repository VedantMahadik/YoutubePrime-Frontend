pipeline {
    agent none
    stages {
        stage('Frontend') {
            agent {
                docker { 
                    label 'windows'
                    image 'node:lts-alpine' 
                }
            }
            steps {
                sh 'node --version'
                sh 'docker build -t gitinnit/jenkins-music-app .'
                sh 'docker run -it -p 8080:8080 --rm --name music-app-1 gitinnit/jenkins-music-app'
            }
        }
    }
}
