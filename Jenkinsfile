pipeline{
	agent any
	stages{
		stage("Pull latest image"){
			steps{
				sh "docker pull automationtesting99/selenium-grid-docker"
			}
		}
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
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			sh "docker-compose down"
		}
	}	
}


