
pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        } // close Build stage

        stage('test') {
            steps {
                echo 'test stage'
                sh 'test -f build/index.html'
            }
        }
    } // close stages
} // close pipeline