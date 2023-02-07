pipeline {
	agent any
	stages {
		stage('Clone git') {
			steps{
				git branch: 'master', url: 'https://github.com/Vancong01/jenkin.git'
			}
		}
		stage('Remote ssh server'){
			steps {
				sshagent(['ssh-remote']) {
    				sh 'ssh -o StrictHostKeyChecking=no -l root 192.168.0.221 touch thuong555.txt'
				}
			}
		}
		
		
	
	}
}
