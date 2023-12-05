pipeline {
    agent any

    stages {
        stage('Run Newman') {
            steps {
                script {
                    // Set paths and variables
                    def collectionPath = ''
                    def environmentPath = ''
                    def testDataPath = ''
                    def delay = 1000
                    def reportFile = ''

                    // Run Newman command with test data
                    bat "\"newman run \"${collectionPath}\" -e \"${environmentPath}\" --iteration-data \"${testDataPath}\" --delay-request ${delay} --reporters html,cli --reporter-html-export \"${reportFile}\""
                }
            }
        }
    }
}
