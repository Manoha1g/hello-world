pipeline{
	agent any
    	tools { 
        	Maven 'maven-3.6.1' 
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
	}
}
