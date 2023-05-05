@Library("ps") _
pipeline {
agent any
environment {
    USER_NAME = "prashant"
}

stages{
 	stage ('clone') {
		steps
			{
			 echo "this job is done by $USER_NAME"
			    sh 'rm -rf *'
			    sh 'git clone https://github.com/psawant27/dotnet-docker.git' 
			   
			}
 	}
	stage ('build') {    
	    steps
			{
                sh 'docker build -t dotnetapp /root/.jenkins/workspace/dot_net/dotnet-docker/samples/aspnetapp/'
			   
			}
 	}
 	stage ('create_container') {    
	    steps
			{
                sh 'docker run -itd -p 90:80 dotnetapp'
			   
			}
 	}
 	stage ('share_libary') {    
	    steps
			{
                echo " this part is to demonstrate variables"
                sawant()
			   
			}
 	}
}
}
