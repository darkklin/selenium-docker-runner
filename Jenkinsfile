pipeline{
	agent any
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d selenium-hub chrome firefox"
			}
		}
		stage("Run The Test"){
			steps{
				sh "docker-compose up search-module book-flight-module"
		   }
		}
		stage("Stop")
		{
			steps{
				sh "docker-compose down"
			}
		}
	}
}