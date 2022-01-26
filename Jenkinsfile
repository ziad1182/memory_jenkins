pipeline {
    agent {
        docker {
            image 'node'
            args '-p 4000:3000'
        }
    }
    stages {
        stage('npm install') {
            steps {
                sh 'npm install'
            }
        }

        stage('install client dependencies') {
            steps {
                sh 'cd client'
            }
            steps {
                sh 'npm install'
            }
        }

        stage('install server dependencies') {
            steps {
                sh 'cd server'
            }
            steps {
                sh 'npm install'
            }
        }
    }
}