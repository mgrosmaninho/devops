pipeline {
  agent any
  stages {
	stage('Docker build') {
	  steps {
		sh 'docker build -t mgrosmaninho/webserver:0.01 /home/manuel/webserver/'
	  }
	}
	stage('Docker push') {
	  steps {
	    sh 'docker push mgrosmaninho/webserver:latest'
	  }
	}
  }
	post {
	  always {
		mail to: 'mgrosmaninho@hotmail.com',
		subject: 'Worked!!!',
		body: 'Website Jenkins pipeline worked'
	  }
	  failure {
	    mail to: 'mgrosmaninho@hotmail.com',
		subject: 'Worked!!!',
		body: 'Website Jenkins pipeline worked'	
	  }
	}
}