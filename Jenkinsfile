pipeline{
    agent any
    
    stages{
        stage("Clone Code"){
            steps{
                echo "Clonning the Code"
                git url:"https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline.git", branch: "main"
            }
        }
        stage("Build"){
            steps{
                echo "Building Image"
                sh "docker build -t note-app-image ."
            }
        }
        stage("Push to Docker Hub"){
            steps{
                echo "Pushing to Docker-Hub"
                withCredentials([usernamePassword(credentialsId:"dockerHub",passwordVariable:"dockerHubPass",usernameVariable:"dockerHubUser")]){
                sh "docker tag note-app-image ${env.dockerHubUser}/note-app-image:v1"    
                sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPass}"
                sh "docker push ${env.dockerHubUser}/note-app-image:v1"
                }
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying the Container"
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
