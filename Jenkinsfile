pipeline {
    agent any
    parameters {
        string (
            name: 'USR_NAME',
            defaultValue: 'knaresh', 
            description: 'Do enter your name'
        )
        booleanParam(
            name: 'SRE_APPROVED',
            defaultValue: true,
            description: 'Is SRE approval taken for this release'            
        )
    }
    stages {
        stage ('Welcome') {
            steps {
                echo "Welcome ${params.USR_NAME}"
                echo "status of approval ${params.SRE_APPROVED}"
            }
        }
    }
}
