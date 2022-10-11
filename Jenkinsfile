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
		stage('sonarscan') {
	    steps{
	            
		            sh 'mvn sonar:sonar \
  -Dsonar.projectKey=jenkins1 \
  -Dsonar.host.url=http://3.110.197.109:9000/sonarqube \
  -Dsonar.login=bdb3555ac768f7d51e8432e73e4440cffe659c93'
			     }
			     }
		}
	        
	}

}	
