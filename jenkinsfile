pipeline {
    agent any

    stages {
        stage ("bulid docker image"){
             steps{
                sh 'docker build -t slack:latest .'
                }
            }
        stage ("test container"){
            steps{
                sh 'docker run -d -p 8081:8081 --name nodeapi slack:latest'
                }
            }
        }
    }