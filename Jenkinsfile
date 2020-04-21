pipeline{
	agent any
	
	stages{
	   stage('checkout'){
	     steps {
		     checkout scm 
		   }}
	   stage('Build'){
	     steps {
		     sh '/home/serevr1/apache-maven-3.6.3/bin/mvn install'
		   }}
	   stage('deploy'){
	     steps {
		     sh 'sshpass -p "server1" scp targget/flipkart-web.war server1@172.17.0.2:/home/server1/apache-tomcat-9.0.33/webapps'
		   }}	    
}
}
