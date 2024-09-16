/* Jenkinsfile */

pipeline {
    agent any
    stages {
        stage("Build Assesement") {
            steps {
                echo "Executing Build ${BUILD_TAG} with URL: ${BUILD_URL}"
                echo "Hello World!"
            }
        }
        stage("Build") {
            steps {
                echo "Build"
            }
        }
        stage("Staging") {
            steps {
                echo "Staging"
            }
        }
        stage("Test") {
            steps {
                echo "Test"
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploy"
            }
        }
    }
}
