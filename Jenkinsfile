pipeline {
    environment {
    registry = "aognov/CI-with-github"
    registryCredential = 'alexisognov'
    dockerImage = ''
    }
    agent any
    stages {
        stage('Building our image') {
            steps{
                sh 'docker build -t  aognov/CI-with-github'
            }
        }
        stage('Test'){
            steps {
                 echo 'Empty'
            }
        }
        stage('Deploy our image') {
            steps{
                echo 'Empty'
            }
        }
    }
}
