pipeline {
agent any


stages{
 	stage ('clone') {
		steps
			{
			   
			    sh 'git clone https://github.com/psawant27/dotnet-docker.git' 
			}
 	}
	stage ('build') {    
	    steps
			{
                sh 'docker build -t dotnetapp /root/.jenkins/workspace/New_Job/dotnet-docker/samples/aspnetapp/'
			   
			}
 	}
 	stage ('create_container') {    
	    steps
			{
                sh 'docker run -itd -p 90:80 dotnetapp'
			   
			}
 	}
}
}
