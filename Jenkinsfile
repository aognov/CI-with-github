pipeline {
    agent any

    stages {
        stage('built') {

                app = docker.build("aognov/CI-with-github")
        }
        stage('test') {
            steps {
                echo 'Testing'
            }
        }
        stage('deploy') {
            docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
                app.push("${env.BUILD_NUMBER}")
                app.push("latest")
            }
        }
      
    }
}
