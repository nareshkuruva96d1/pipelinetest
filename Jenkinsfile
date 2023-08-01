pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                // echo "Building !!!"
                error ("Build Failed")
            }
        }
    }
    post {
        success {
            echo "Post Build ==> Success is called"
        }
        failure {
            echo "Post Build ==> Failure is called"
            // body, can be any code
            // mailer ==> SRE
        }
        always {
            echo "Post Build ==> Always is called"
        }
    }
}
