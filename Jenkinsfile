pipeline{
    agent any
    tools{
        nodejs "NodeJs"
    }
    stages{
        stage("Checkout"){
            steps{
                checkout scm
            }
        }
        stage("Install Dependencies"){
            steps{
                bat "npm install"
            }
        }
        stage("Test"){
            steps{
                echo "Tested"
              //  bat "npm test"
            }
        }
        stage("Build"){
            steps{
                bat "npm run build"
            }
        }
       

       
    }
}