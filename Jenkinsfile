//SCRIPTED
//DECLARATIVE
pipeline {
	agent any
	//agent { docker { image 'maven:3.8.4'} }
	//agent { docker { image 'node:17.4'} }
	environment {
		dockerhome = tool 'Mydocker'
		mavenhome = tool 'Mymaven'
		path = "$dockerhome/bin:$mavenhome/bin:$path"
	}


	stages {
		stage('checkout') {
			steps {
			  sh 'mvn --version'
			  sh 'docker --version'	
			  echo "Build"
			  echo "path - $path"
			  echo "Build_number - $env.Build_number"
			  echo "Build_id - $env.Build_id"
			  echo "Job_name - $env.Job_name"
			  echo "Build_tag - $env.Build_tag"
			  echo "Build_url - $env.Build_url"
	        }
		}
		stage('compile') {
			steps {
			  sh "mvn clean compile"
			}
		}
		stage('test') {
			steps {
			  sh "mvn test"
			}
		}
		stage('Integration test') {
			steps {
			  sh "mvn failsafe:integration-test failsafe:verify"
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
