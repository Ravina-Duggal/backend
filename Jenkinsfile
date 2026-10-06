pipeline{
    agent any
    stages{
        stage("clone repo"){
            steps{
                git url:"", branch:"main"
            }
        }
        stage("build"){
            steps{
                sh "docker build -t backend ."
            }
        }
        stage("run"){
            steps{
                sh "docker run -d -p 5000:5000 backend"
            }
        }
    }
}