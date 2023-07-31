pipeline {
    agent any
    environment {
        DEPLOY_TO = "knaresh" // static, hard
    }
    stages {
        stage ('Example Build') {
            steps {
                echo "Executing stage !!!!!!"
            }
        }
        stage ('Deploy') {
            when {
                anyOf {
                    expression {
                        BRANCH_NAME ==~ /(production|staging)/
                    }
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "Deploying in Prod Env"
            }

        }
    }
}
