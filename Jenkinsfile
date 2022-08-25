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
//         stage("Deploy to test"){
//             when {
//                 branch "develop"
//             }
//             steps{
//                 echo "deploying to development server"
//             }
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

