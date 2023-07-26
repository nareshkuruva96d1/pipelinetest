pipeline {
    agent any
    environment {
        DEPLOY_TO = 'productions'
    }
    stages {
        stage('When Example'){
            when {
                not {
                    equals expected: "productions", actual: "${DEPLOY_TO}"
                }
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
    }
}
