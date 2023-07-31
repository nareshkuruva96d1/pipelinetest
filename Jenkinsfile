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
                stage ('sonar scan') {
                    steps {
                        echo "******Performing Sonar Scans******"
                        sleep 10
                    }
                }    
                    stage ('Fortify'){
                        steps {
                            echo "******Performing Fortify Scans******"
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
