pipeline{
	agent any 
	stages{
		stage("Run Test"){
			steps{
				bash "docker-compose up"
			}
		}
		stage("Bring Grid Down"){
			steps{
				bash "docker-compose down"
			}
		}

	}
}