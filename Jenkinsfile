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
        stage("Deployment"){
            steps{
                    bat "delete /q /s c:\\inetpub\\wwwroot\\react\\*"
                    bat "xcopy /E /I /Y build\\* c:\\inetpub\\wwwroot\\react\\"
            }
        }
       

       
    }
}