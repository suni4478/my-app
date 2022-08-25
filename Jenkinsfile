@Library("libres") _
pipeline{
    agent any 
    stages{
        stage("git checkout"){
            steps{
                git credentialsId: 'devtest', url: 'https://github.com/suni4478/my-app.git'
            }
        }
        stage("maven deploy"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("tomcat deploy"){
            steps{
                 tomcatdeploy("172.31.18.255","ec2-user",'pipeline-dev-exec')
            }
        }
    }
}
