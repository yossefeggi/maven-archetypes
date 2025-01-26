pipeline {
    agent any
    parameters {
        // Define a choice parameter for Maven commands
        choice(
            name: 'MAVEN_COMMAND',
            choices: ['install', 'package', 'clean', 'test'],
            description: 'Choose a Maven command to execute'
        )
    }
    stages {
        // A stage for executing the chosen Maven command
        stage('Build') {
            steps {
                echo "Selected Maven Command: ${params.MAVEN_COMMAND}"
                // Execute the chosen Maven command
                sh "mvn ${params.MAVEN_COMMAND}"
            }
        }
    }
}

