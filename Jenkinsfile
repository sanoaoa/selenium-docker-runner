pipeline{
	agent any
		stages{
			stage("Start Grid"){
				steps{
					sh "docker-compose up -d --scale chrome=4 hub chrome firefox"
				}
			}
			stage("Run Test"){
				steps{
				sh "docker-compose up TestRun"
				}	
			}
			stage("Stop Grid"){
				steps{
				sh "docker-compose down"
				}	
			}
		}
	
}