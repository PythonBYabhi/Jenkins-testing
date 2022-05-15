pipeline {

agent any

stages {
	stage('SCM') {
		when {
			branch 'main'
		}
		steps  {
			echo "git pull my code for java app"
			checkout([
				$class: 'GitSCM', 
				branches: [[
					name: '*/main'
				]], 
				extensions: [], 
				userRemoteConfigs: [[
					url: 'https://github.com/abhi-dev91/Jenkins-testing.git'
				]]
	        	]
		)
			
			
		}
	}

	stage('Build') {
		steps { 
			echo "hello from build"
		}
	}	

	stage('Deploy') {
		steps {
			echo 'java -jar target/*.jar'
		}
	}

	stage('Deploy to Prod') {
		steps {
			echo "my final webapp to prod"
		}
	}

}

}
