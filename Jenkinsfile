pipeline {
    agent {
        docker {
            image 'node'
            args '-p 3000:3000'
        }
    }
    stages {
        satge('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}