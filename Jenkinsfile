pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.0.2', '2.0', '3.0', '4.50'], description: 'Select the version to build')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Execute tests?')
    }

    stages {
        stage("Build") {
            steps {
                echo "I am building version ${params.VERSION}"
                // Add your build steps here
            }
        }
        
        stage("Test") {
            when {
                expression {
                    params.executeTests == true
                }
            }
            steps {
                echo "I am testing version ${params.VERSION}"
                // Add your test steps here
            }
        }

        stage("Deploy") {
            steps {
                echo "I am deploying version ${params.VERSION}"
                // Add your deployment steps here
            }
        }
    }
}
