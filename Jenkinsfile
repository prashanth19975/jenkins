pipeline {
    agent any
    stages {
        stage('git clone') {
            steps {
			   git branch: 'main', url: 'https://github.com/prashanth19975/jenkins.git'
             }
             }
		stage('maven version') {
            steps {	 
			    sh 'mvn --version'
				}
				}
	    stage('maven clean') {
            steps {	 
			    sh 'mvn clean'
				}
				}			
		stage('maven validate') {
            steps {	 
			    sh 'mvn validate'
				}
				}		
		stage('maven compile') {
            steps {	 
			    sh 'mvn compile'
				}
				}		
		stage('maven test') {
            steps {	 
			    sh 'mvn test'
				}
				}		
                stage('maven package') {
            steps {	 
			    sh 'mvn package'
				}
				}
		stage('sonarqube analysis') {
	    steps{
	    withsonarQubeEnv('sonarqube-8.9.9'){
	                     sh 'mvn sonar:sonar'
			     }
			     }
		}
	        
	}

}	
