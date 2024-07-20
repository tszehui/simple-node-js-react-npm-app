pipeline {
	agent any
	stages {
    		stage('Build') {
        		steps {
            			nodejs('nodejs'){
                			sh 'npm install && npm install cross-env'
            			}
        		}
    		}
	
		stage('Test') {
	            steps {
	                sh './jenkins/scripts/test.sh'
	            }
	        }
	}
}
