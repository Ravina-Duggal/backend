pipeline{
    agent any
    stages{
        stage("clone repo"){
            steps{
                git url:"https://github.com/Ravina-Duggal/backend.git", branch:"main"
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
                // sh "docker run -d -p 5000:5000 ravinaduggal/backend:latest"
            }
        }
    }
}