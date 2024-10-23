pipeline{
    agent any
    stages{
        stage("npm install"){
            steps{
               bat 'npm install'
            }
        }
        parallel {
            stage("run npm audit tests"){
                steps{
                bat 'npm audit'
                }
            }
            stage("execute tests"){
                steps{
                bat 'npm test'
                }
            }
        }
    }
}