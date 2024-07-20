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
	}
}
