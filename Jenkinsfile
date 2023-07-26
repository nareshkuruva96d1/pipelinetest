pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('When Example'){
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }

            }
            steps {
                echo "all conditons satisfied"
            }
        }
        stage ('Secondstage') {
            steps {
                echo "execute, irrespective of the condition"
            }
        }
    }
}
