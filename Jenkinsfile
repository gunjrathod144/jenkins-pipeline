pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'building'
            }
        }

        stage('Test') {
            parallel {

               stage('approve') {
                   steps{
                       input message: 'Test passed. Deploy to production?'
                   }
               }

                stage('Deploy'){
                    steps{
                        sh 'echo deploying to production'
                    }
                }
                
                stage('Integration') {
                    steps {
                        sh 'echo Running integration tests'
                    }
                }
            }
        }
    }
}
