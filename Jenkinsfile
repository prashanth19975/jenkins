node {
    def mvnHome
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git credentialsId: '7055e685-65e1-4ff3-a369-6085c5f4ca7c', url: 'https://github.com/prashanth19975/prashanth19975.git'
        git branch: 'main', credentialsId: '7055e685-65e1-4ff3-a369-6085c5f4ca7c', url: 'https://github.com/prashanth19975/jenkins.git'
        // Get the Maven tool.
        // ** NOTE: This 'M3' Maven tool must be configured
        // **       in the global configuration.
     }
    stage('mvn version') {
        // Run the maven build
        sh 'mvn --version'		
     }
    stage('mvn clean') {
        // Run the maven build
        sh 'mvn clean'
     }
    stage('mvn validate') {
        // Run the maven build
        sh 'mvn validate'
     }
    stage('mvn compile') {
        // Run the maven build
        sh 'mvn compile'
     }
    stage('mvn test') {
        // Run the maven build
        sh 'mvn test'
     }
    stage('mvn package') {
        // Run the maven build
        sh 'mvn package'
     }
}