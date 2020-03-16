pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            sh './mvnw package'
            }
        }

post {
    success {
        mail to: 'b_julia@live.com',
             subject: "Successful Pipeline: ${currentBuild.fullDisplayName}",
             body: "All went well with ${env.BUILD_URL}"
    }
}
}
