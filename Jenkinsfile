pipeline{
    agent any
    stages{
        stage("npm install"){
            steps{
               bat 'npm install'
            }
        }
         stage("execute tests"){
            steps{
               bat 'npm test'
            }
        }
    }
}