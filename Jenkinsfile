pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('When Example'){
            When {
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
    }
}
