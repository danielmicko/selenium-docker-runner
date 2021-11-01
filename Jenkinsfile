pipeline{
	agent any 
	stages{
		stage("Grid Compose Up"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Tests"){
			steps{
				bat "docker-compose up search-module book-flight-module"
			}
		}
		stage("Grid Teardown"){
			steps{
				bat "docker-compose down"
			}
		}

	}
}
