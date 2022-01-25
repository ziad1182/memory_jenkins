pipeline {
    agent {
        docker {
            image 'node'
            args '-p 4000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'cd client'
                sh 'npm install'
                sh 'cd server'
                sh 'npm install'
            }
        }
    }
}