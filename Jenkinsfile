pipeline {
	agent any
	stages{
		stage('Build'){
			steps{
				echo 'Building'
				powershell(returnStdout: true, script: '.\\BuildandDeploy.ps1')
			}
		}
	}
}
