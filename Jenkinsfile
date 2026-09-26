pipeline{
    agent any
parameters {
    choice(name: 'ENVIRONMENT', choices: ['staging', 'prodcution'], description: 'Target')
}
    stages{
      stage('Test') {
          parallel {
              stage('unit') { steps { sh 'echo unit tests' } }
              stage('Integration') { steps { sh 'echo Integration tests' }}
          }
      }
        
