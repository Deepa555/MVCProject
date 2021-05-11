pipeline {
    agent any 
        stage('Build') { 
            steps {
                echo 'Building..'
                bat '"C:\Program Files (x86)\MSBuild\14.0\Bin\msbuild\" BuildTest.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"
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
