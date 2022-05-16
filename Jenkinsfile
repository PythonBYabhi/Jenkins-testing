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
			branch 'main'
		}
		steps {
			echo "hello from SCM"
		}
		// steps  {
		// 	echo "git pull my code for java app"
		// }
	}

	stage('Build') {
		when {
			branch 'main'
    }
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
