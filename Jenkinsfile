pipeline{
    agent any
    stages{
        stage("npm install"){
            steps{
               bat 'npm install'
            }
        }
        stage("parallel execution"){
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
        stage("Deploy to staging"){
            steps{
                echo "Deploy to staging"

            }
        }
        stage("Approval for production deploymenet"){
            steps{
                input message: "Approve deployment for production?", ok: "Deploy"
            }
        }
        stage("Deploy to production"){
            steps{
                 echo "Deploy to production"
            }
        }
    }
}