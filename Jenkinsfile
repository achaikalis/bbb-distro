/* Jenkinsfile */

pipeline {
    
    agent any
    
    environment {

        SERVER_CREDENTIALS = credentials("Global")

    }
    
    stages {
    
        stage("Build Assesement") {
    
            echo "Executing Build ${BUILD_TAG} with URL: ${BUILD_URL}"
    
            echo "Hello World!"
    
        }
        stage("Build") {
            
            echo "Build"
        
        }

        stage("Staging") {
                
            withCredentials([
                usernamePassword(credentials: Global, usernameVariable: USER, passwordVariable: PWD)
            ]) {
                echo "Staging"
            }
        
        }
        
        stage("Test") {
        
            echo "Test"
        
        }
        
        stage("Deploy") {
        
            echo "Deploy"
        
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
