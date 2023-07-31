pipeline {
    agent any
    parameters {
        string (
            name: 'USR_NAME',
            defaultValue: 'knaresh', 
            description: 'Do enter your name'
        )
    }
    stages {
        stage ('Welcome') {
            steps {
                echo "Welcome ${params.USR_NAME}"
            }
        }
    }
}
