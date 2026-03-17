pipeline {
    agent any

    stages {
        stage('Parallel Demo') {
            parallel {

                stage('Job A') {
                    steps {
                        echo "Hello from Job A"
                        echo "Job A is running in parallel"
                    }
                }

                stage('Job B') {
                    steps {
                        echo "Hello from Job B"
                        echo "Job B is also running in parallel"
                    }
                }

            }
        }
    }
}