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
        stage (Deploy) {
            when {
               allOf {
                    branch: 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "Deploying in Prod Env"
            }

        }
    }
}
