pipeline {
    environment {
    registry = "aognov/CI-with-github"
    registryCredential = 'alexisognov'
    dockerImage = ''
    }
    agent any

    stage('Building our image') {
        steps{
            script {
                dockerImage = docker.build registry + ":$BUILD_NUMBER"
            }
        }
    }
    stage('Test'){
        steps {
             echo 'Empty'
        }
    }
    stage('Deploy our image') {
        steps{
            script {
                docker.withRegistry( '', registryCredential ) {
                    dockerImage.push()
                }
            }
        }
    }
}
