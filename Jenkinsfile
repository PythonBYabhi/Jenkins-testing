pipeline {

agent any

stages {
	stage('SCM') {
		steps  {
			echo "git pull my code for java app"
			
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
