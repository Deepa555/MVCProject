pipeline {
    agent any 
        stage('Build') { 
            steps {
                echo 'Building..'
                powershell(returnStdout: true, script: '.BuildandDeploy.ps1')	
            }
        }
        stage('Publish') { 
            steps {
                bat 'dotnet publish BuildTest/WebApplication1'
            }
        }
        stage('Clean up') { 
            steps {
                bat 'rmdir /Q /S BuildTest'
            }
        }
    }
}
