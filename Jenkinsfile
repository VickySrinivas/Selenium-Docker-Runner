pipeline{
	agents any
	stages{
		stage("Run Tests"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bring down Grid"){
			steps{
				sh "docker-compose down"
			}
		}
	}

}