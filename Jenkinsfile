pipeline {
agent any


parameters {
	string(
		defaultValue: 'main', 
		name: 'branch_name', 
		trim: true
	)
}
stages {
	stage('SCM') {
		when {
			branch '${branch_name}'
		}
		steps {
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
		// steps  {
		// 	echo "git pull my code for java app"
		// }
	}

	stage('Build') {
		steps { 
			sh 'echo "hello from build"'
		}
	}	

	stage('Deploy') {
		steps {
			sh 'echo "java -jar target/*.jar"'
		}
	}

	stage('Deploy to Prod') {
		steps {
			sh 'echo "my final webapp to prod"'
		}
	}

}

}
