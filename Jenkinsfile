pipeline{
    agent any
    stages{
        stage("maven build"){
            when {
                branch "develop"
            }
            steps{
                sh "mvn package"
            }
        stage("Deploy to production"){
            when {
                branch "master"
            }
            steps{
                echo "deploying to master server"
            }
        }
    }
}

