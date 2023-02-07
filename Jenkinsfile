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
				echo '1.................................'
    				sh 'ssh -o StrictHostKeyChecking=no -l vsii 192.168.0.221 docker ps'
				echo '2.................................'
				sh 'ssh -o StrictHostKeyChecking=no -l vsii 192.168.0.221 docker version'
				}
			}
		}
		
		
	
	}
}
