pipeline{
	agent any{
		stages{
			stage("Start Grid"){
				steps{
					sh "docker-compose up -d hub chrome firefox"
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