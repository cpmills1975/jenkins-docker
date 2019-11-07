pipeline {
	agent any

	stages {
		stage('Clone repo') {
			checkout scm
		}

		stage('Build image') {
			app = docker.build("cpmills/jenkins-docker")
		}

		stage('Test image') {
			app.inside {
				sh 'echo "Need to define some tests here!"'
			}
		}

		stage('Push image') {
			sh 'echo "Need to push image somewhere here!"'
		}
	}
}
