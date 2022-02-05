//SCRIPTED
//DECLARATIVE
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
			  sudo 'mvn --version'	
			  echo "Build"
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
