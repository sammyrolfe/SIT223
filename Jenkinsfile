pipeline {
    agent any
    environment {
        DIRECTORY_PATH= "~/Desktop/BigSoftwareProject/Builds"
        TESTING_ENVIRONMENT= "SIT223 Test Environment"
        PRODUCTION_ENVIRONMENT= "SIT223 Production Environment"
    }
    stages {
        stage('Build') {
            steps {
                echo "fetch the source code from the $DIRECTORY_PATH"
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
                echo "deploy application to $TESTING_ENVIRONMENT"
            }
        }
        stage('Approval') {
            steps {
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "deploy application to $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}