pipeline {
    agent any

    stages {
        stage('Parallel Demo') {
            parallel {

                stage('Job A1') {
                    steps {
                        echo "Hello from Job A1"
                        echo "Job A1 is running in parallel"
                    }
                }

                stage('Job B1') {
                    steps {
                        echo "Hello from Job B1"
                        echo "Job B is also running in parallel"
                    }
                }

            }
        }
    }
}