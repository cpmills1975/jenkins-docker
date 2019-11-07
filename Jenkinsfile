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
				app = docker.build("cpmills/jenkins-docker")
			}
		}

		stage('Test image') {
			steps {
				app.inside {
					sh 'echo "Need to define some tests here!"'
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
