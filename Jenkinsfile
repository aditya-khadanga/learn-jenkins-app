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
                    if npm run | grep -q " build"; then
                        npm run build
                    else
                        echo "No build script found in package.json, skipping build step."
                    fi
                    ls -la
                                '''
            }
        }
    }
        }
    }
}