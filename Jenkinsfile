pipeline{
	agent any
	stages{
		stage('scm checkout'){
			steps{
				git url: 'https://github.com/Manoha1g/hello-world.git'
			}
		}
		stage('maven Build'){
			steps{
			//	buildInfo = goals: 'clean install'
				sh 'mvn install'
			}
		}
	}
}
