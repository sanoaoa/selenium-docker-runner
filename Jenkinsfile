pipeline{
	agent any
		stages{
			stage("Start Grid"){
				steps{
					sh " sudo docker-compose up -d hub chrome firefox"
				}
			}
			stage("Run Test"){
				steps{
				sh " sudo docker-compose up TestRun"
				}	
			}
			stage("Stop Grid"){
				steps{
				sh "sudo docker-compose down"
				}	
			}
		}
	
}