//SCRIPTED
//DECLARATIVE
pipeline {
	agent any
	//agent { docker { image 'node:17.4'} }
	stages {
		stage('Build') {
			steps {
			  //sh 'mvn --version'
			  //sh 'node --version'	
			  echo "Build"
			  echo "path - $path"
			  echo "Build_number - $env.Build_number"
			  echo "Build_id - $env.Build_id"
			  echo "Job_name - $env.Job_name"
			  echo "Build_tag - $env.Build_tag"
			  echo "Build_url - $env.Build_url"
	        }
		}
		stage('Test') {
			steps {
			  echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
			  echo "Integration Test"
			}
		}
	} 
	
	post {
		always {
			echo 'i am awesome. i run aways'
		}
		success {
			echo 'i run when u are successful'
		}
		failure {
			echo 'i run when u fail'
		}
	}
}
