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

                stage('Unit') {
                    steps {
                        sh 'echo Running unit Tests'
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
