@Library('sharedLibraryCi@master')_
pipeline{
	agent any
    	tools { 
        	maven 'maven-3.6.1' 
	 }
	environment {
		name = "test-env-name"
//		commitId = gitCommitId()
	}
	stages{
		stage('scm checkout'){
			steps{
//			git credentialsId: 'github', url: 'https://github.com/Manoha1g/hello-world.git'
			checkout-stage(
				branch: "master"
				url: "https://github.com/Manoha1g/hello-world.git"
			)
			}
		}
		stage('maven build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('test'){
			steps{
				echo "Please find the below worspace path:"
				echo "${workspace}"
				echo "${name}"
			//	environment {
			//		name = 'test-stage-name'
			//		author = "test-author"
			//		echo "${name}"
			//		echo "${author}"
			//	}
			}
		}
		stage('set Build Number'){
			steps{
				script{
					currentBuild.displayName = "#--hello-world-"+currentBuild.number
				}
//				echo ${commitId}
			}
		}
	}
}
def gitCommitId(){
	def latestCommitId = sh script: '''git rev-parse --short HEAD''', returnStdio: true
	return latestCommitId
}
