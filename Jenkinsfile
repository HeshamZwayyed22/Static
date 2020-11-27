pipeline {
    agent any
    stages {
      stage(‘Upload to AWS’) {
        steps {
		           withAWS(region:'us-west-2', credentials:'aws-static') {	   
                          s3Upload(file:'index.html', bucket:'aws-jenkins-pipeline', path:'index.html')
		}
		
			    sh ‘echo "Hello World"’
			    sh '''
				      echo "Multiline shell steps work too"
				      ls -lah
			    '''
          
          }
        }
      }
    }
