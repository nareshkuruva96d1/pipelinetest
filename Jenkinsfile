pipeline {
    agent any
    stages {
        stage('When Example') {
            when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
        stage ('Secondstage') {
            steps {
                echo "execute, irrespective of the condition"
            }
        }
    }
}
