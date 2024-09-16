/* Jenkinsfile */

pipeline {
    
    agent any
    
    environment {

        SERVER_CREDENTIALS = credentials("Global")

    }
    
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

            withCredentials([
                usernamePassword(credentials: Global, usernameVariable: USER, passwordVariable: PWD)
            ]) {
                echo "Staging"
            }

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
    
    post {
    
        success {
    
            /* Email Notification with oe-build-perf-report contents */
    
            /* Email Notification with QEMU / LAVA report summary */
    
        }
    
        failure {
    
            /* Email Notification with BitBake error logs */
    
            /* Email Notification with QEMU / LAVA error logs */
    
        }
    }
}
