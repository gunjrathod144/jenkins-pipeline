stage('Test') {
    parallel {
        stage('unit') {
            steps {
                sh 'echo Running unit Tests'
            }
        }
        stage('Integration'){
            steps{
                sh 'echo running integration tests'

            }
        }
    }
}
        
