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
			
		}
		post{
			always{
				archiveArtifacts artifacts:'output/**'
				sh "docker-compose down"
			
			}
		}
	
}