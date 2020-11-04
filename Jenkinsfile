pipeline{
	agent any
	stages{
		stage("Run Grid"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run tests"){
			steps{
				sh "docker-compose up searchPageTest bookflightTest"
			}
		}
		stage("Bring down Grid"){
			steps{
				sh "docker-compose down"
			}
		}
	}

}