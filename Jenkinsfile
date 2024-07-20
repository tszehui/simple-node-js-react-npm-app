pipeline {
	agent any
	stages {
    		stage('Build') {
        		steps {
            			nodejs('nodejs'){
                			sh 'npm install'
            			}
        		}
		}
		 stage('Dependency-Check') {
            		steps {
                		dependencyCheck additionalArguments: '''
                    		-o './'
                    		-s './'
                    		-f 'ALL'
                    		--prettyPrint
                    		--nvdApiKey ${NVD-API-KEY}
                		''', odcInstallation: 'OWASP Dependency-Check Vulnerabilities'
                
                		dependencyCheckPublisher pattern: 'dependency-check-report.xml'
            		}
        	}

	}
}
