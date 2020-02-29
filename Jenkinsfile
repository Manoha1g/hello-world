pipeline{
	agent any
    	tools { 
        	maven 'maven-3.6.1' 
	 }
	stages{
		stage('scm checkout'){
			steps{
				git url: 'https://github.com/Manoha1g/hello-world.git'
			}
		}
		stage('maven build'){
			steps{
				sh 'mvn clean install'
			}
		}
		//stage('test'){
		//	steps{
		//		echo "Please find the below worspace path:"
		//		echo "${workspace}"
			//environment {
			//	name = 'test-stage-name'
			//	author = "test-author"
		//		}
		//	}
		//}
	}
}
