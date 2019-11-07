pipeline {
	agent any

	stages {
		stage('Clone repo') {
			steps {
				checkout scm
			}
		}

		stage('Build image') {
			steps {
				script {
					app = docker.build("cpmills/jenkins-docker")
				}
			}
		}

		stage('Test image') {
			steps {
				script {
					app.inside {
						sh 'echo "Need to define some tests here!"'
					}
				}
			}
		}

		stage('Push image') {
			steps {
				sh 'echo "Need to push image somewhere here!"'
			}
		}
	}
}
