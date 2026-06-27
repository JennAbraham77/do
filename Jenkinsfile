pipeline {
	agent any
	stages {
		stage('Build'){
			steps{
				sh 'docker build -t do .'
			}
		}
		stage('Test'){
			steps{
				sh 'echo testing'
			}
		}
		stage('Push'){
			steps{
				sh 'docker tag abc jennabraham77/do'
				sh 'docker push jennabraham77/do'
			}
		}
		stage('Deploy'){
			steps{
				sh 'docker run -d -p 8081:80 jennabraham77/do'
			}
		}
	}
}
