    pipeline {
        agent any
        stages {
            stage ('Build'){
                steps {
                    echo "Building node application"
                }
            }
            stage ('Deploy to Prod') {
                options {
                    timeout (time: 30, unit: 'SECONDS')
                }
                input {
                    message: "Should i continue ??",
                    ok "Approved",
                    submitter "nijira",
                    submitterParametr "whoapproved"
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
                            choices: 'Regular\nHotfix',
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
                }
                steps {
                    echo "Deploying to Production"
                    echo "Welcome ${params.USR_NAME}"
                    echo "status of approval ${params.SRE_APPROVED}"
                    echo "This is a ${params.Release} Release"
                    echo "Approved by this person: ${whoapproved}"                
                }

            }
        }
    }
