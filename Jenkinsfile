pipeline {
    agent any
    
    stages {
        
        stage("code"){
            steps{
                git url: "https://github.com/hirenrparghi/DevSecOps-Node-todo-cicd-Project.git", branch: "master"
                echo 'code cloned'
            }
        }
        stage("build and test"){
            steps{
                sh "docker build -t node-app-test-new ."
                echo 'code build also done'
            }
        }
        // stage("scan image"){
        //     steps{
        //         echo 'image is scanned'
        //     }
        // }
        // stage("push"){
        //     steps{
        //         withCredentials([usernamePassword(credentialsId:"dockerHub",passwordVariable:"dockerHubPass",usernameVariable:"dockerHubUser")]){
        //         sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPass}"
        //         sh "docker tag node-app-test-new:latest ${env.dockerHubUser}/node-app-test-new:latest"
        //         sh "docker push ${env.dockerHubUser}/node-app-test-new:latest"
        //         echo 'image is pushed'
        //         }
        //     }
        // }
        // stage("deploy"){
        //     steps{
        //         sh "docker-compose down && docker-compose up -d"
        //         echo 'deployment is completed'
        //     }
        // }
    }
}
