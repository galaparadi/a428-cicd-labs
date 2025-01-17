node {
    def appDockerImage = docker.image('node:16-buster-slim')
    appDockerImage.withRun('-p 3000:3000') { container ->
        stage('Build') {
            sh 'npm install'
        }
        
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
}

