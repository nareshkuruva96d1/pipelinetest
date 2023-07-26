pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('When Example'){
            when {
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
    }
}
