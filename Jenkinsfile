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
                    environment name: 'DEPLOY_TO', value: 'knaresh'
                }
            }
            steps {
                echo "Deploying in Non-Prod Env"
            }

        }
        stage ('Prod') {
            when {
                //buildingTag()
                // buildingTag will execute when we are building a tag 
                // tag will execute only when we are executing a specific tag
                // tag "release-*"
                // vx.x.x, v1.2.3
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP" 
            }
            steps {
                echo "Deploying to prod Kubernetes cluster"
            }
        }
    }
}
