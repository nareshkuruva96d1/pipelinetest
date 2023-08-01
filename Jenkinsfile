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
        choice(
            choices: 'Regular\Hotfix',
            description: "What sort of release is this, Regular release or Hotfix ?",
            name: 'Release'           
        )
        text(
            name: 'Notes',
            defaultValue: "Enter Release notes",
            description: "Do Enter the description"
        )
        credentials(
            name: 'mycredentials',
            description: "mycredentials",
            required: true
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
