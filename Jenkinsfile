@Library("libres") _
pipeline{
    agent any 
    stages{
        stage("maven deploy"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("tomcat deploy"){
            when{
                branch "develop"
            }
            steps{
                 tomcatdeploy("172.31.18.255","ec2-user",'pipeline-dev-exec')
            }
        }
        stage("master deploy"){
            when{
                branch "master"
            }
            steps{
                 tomcatdeploy("172.31.18.255","ec2-user",'pipeline-dev-exec')
            }
        }
    }
}
