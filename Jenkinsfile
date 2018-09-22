pipeline {
    stages {

        stage('Docker build'){
            steps{
                docker.build('demo')
            }
        }

        stage('Docker push'){
            steps{
                docker.withRegistry('https://003656774475.dkr.ecr.us-east-1.amazonaws.com', 'ecr:us-east-1:demo-ecr-credentials') {
                    docker.image('demo').push('latest')
                }
            }
        }
    }
}