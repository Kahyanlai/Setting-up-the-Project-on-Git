pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/path/to/code'
        TESTING_ENVIRONMENT = 'testing'
        PRODUCTION_ENVIRONMENT = 'Kahyanlai'
    }

    stages {
        stage('Build') {
            steps {
                echo "fetch the source code from the directory: ${DIRECTORY_PATH}"
                echo "compile the code and generate any necessary artifacts"
            }
        }

        stage('Test') {
            steps {
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "deploy the application to a testing environment: ${TESTING_ENVIRONMENT}"
            }
        }

        stage('Approval') {
            steps {
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "deploying the code to production environment: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}