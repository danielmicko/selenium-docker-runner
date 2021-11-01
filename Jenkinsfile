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
				bat "docker-compose up search-module-chrome search-module-firefox bookflight-module"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			bat "docker-compose down"
		}
	}
}
