pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                timeout (time: 300, unit: 'SECONDS') {
                input message: "Do you like to Build", ok: "yes", submitter: 'nijira'
                }
                echo "Building the application"
            }
        }
    }
}
