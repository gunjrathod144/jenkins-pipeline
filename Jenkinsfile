pipeline{
    agent any
parameters {
    choice(name: 'ENVIRONMENT', choices: ['staging', 'prodcution'], description: 'Target')
}
    stages{
        stage('Deploy') {
            steps{
                sh "echo Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
