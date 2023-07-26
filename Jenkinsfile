pipeline {
    agent any
    environment {
        DEPLOY_TO = 'new'
    }
    stages {
        stage('When Example'){
            when {
                not {
                    equals expected: "productions", actual: "${DEPLOY_TO}"
                }
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
    }
}
