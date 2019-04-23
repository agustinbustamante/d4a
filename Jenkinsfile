pipeline{
	agent any 
	stages{
		stage('Initial Setup'){
			steps{
				sh 'echo Starting...'
			}
		}
		stage('Checking Docker'){
			steps{
				sh 'sudo docker ps'
			}
		}
		stage('cd home bkcp'){
			steps{
				sh 'sudo cd /home/backup/'
			}
		}
		stage('Build Docker'){
			steps{
				sh 'sudo docker build --tag=ndeah .'
			}
		}
		stage('Deploy Container'){
			steps{
				sh 'sudo docker run -p 80:80 --name ndeahepic -rm ndeah'
			}
			
		}
	}
}
