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
  -Dsonar.projectKey=project1 \
  -Dsonar.host.url=http://3.110.62.244:9000/sonarqube \
  -Dsonar.login=11baad226d79ef647a58fffc535e8656c8340f57'
			     }
		             }
	       stage('maven deploy') {
            steps {	 
			    sh 'mvn deploy'
				}
				}  
              stage('tomcat deploy') {
	    steps {
		      sshagent(['TOMCAT']) {
                   // some block
                            sh 'scp -o StrictHostkeyChecking=no webapp/target/webapp.war ec2-user@13.235.50.153:/root/apache-tomcat-10.0.27/webapps'
		      }
	    }
	}
    
}

}	
