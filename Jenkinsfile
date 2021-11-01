pipeline{
	agent any 
	stages{
		stage("Run Test"){
			steps{
				sh "#!/bin/bash docker-compose up"
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "#!/bin/bash docker-compose down"
			}
		}

	}
}