pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['staging', 'production'],
            description: 'Target'
        )
    }

    stages {

        stage('Test') {
            parallel {

                stage('Unit') {
                    steps {
                        sh 'echo unit tests'
                    }
                }

                stage('Integration') {
                    steps {
                        sh 'echo Integration tests'
                    }
                }
            }
        }

        stage('Approve') {
            steps {
                input message: 'Deploy to production?'
            }
        }
    }

    post {
        success {
            echo 'pipeline succeeded'
        }

        failure {
            echo 'pipeline failed'
        }
    }
}
