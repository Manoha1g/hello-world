pipeline{
	agent any
    	tools { 
        	maven 'maven-3.6.1' 
	 }
	environment {
		name = "test-env-name"
	}
	stages{
		stage('scm checkout'){
			steps{
				git credentialsId: 'github', url: 'https://github.com/Manoha1g/hello-world.git'
			}
		}
		stage('maven build'){
			steps{
				sh 'mvn clean install'
			}
		}
	environment {
		author = "test-author-name"
	}
		stage('test'){
			steps{
				echo "Please find the below worspace path:"
				echo "${workspace}"
				echo "${name}"
				echo "${author}"
			//environment {
			//	name = 'test-stage-name'
			//	author = "test-author"
			//	echo "${name}"
			//	}
			}
		}
	}
}
