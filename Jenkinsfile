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
            steps{
                 tomcatdeploy("172.31.18.255","ec2-user",'pipeline-dev-exec')
            }
        }
    }
}
