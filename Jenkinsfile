// parallel stages
pipeline {
    agent any
    stages {
        stage ('Build'){
            steps {
                echo "Building Maven Application"
            }
        }
        stage ('Scans') {
            parallel {
                failfast true
                stage ('sonar scan') {
                    steps {
                        echo "******Performing Sonar Scans******"
                        sleep 10
                    }
                }    
                    stage ('Fortify'){
                        steps {
                            echo "******Performing Fortify Scans******"
                            error "Trying to recreating the error message"
                            sleep 10
                        }
                    }
                    stage ('Trivy'){
                        steps {
                            echo "******Performing Container Scans******"
                            sleep 10
                        }
                    }
            }
        }
        stage ('Deploy') {
            steps {
                echo "Deploying to env"
            }
        }
    }
}
