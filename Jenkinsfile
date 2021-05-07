pipeline {
    agent any 
    stages {
        stage('Restore') { 
            steps {
                bat 'dotnet restore BuildTest/WebApplication1'
            }
        }
        stage('Build') { 
            steps {
                bat 'dotnet build BuildTest/WebApplication1'
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
