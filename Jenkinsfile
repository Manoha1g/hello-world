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
		stage('test'){
			environment {
				name = "test-stage"
				author = 'test-author'
			}
		}
	}
}
