node {
    def mvnHome
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git branch: 'main', credentialsId: 'gitjenkins', url: 'https://github.com/prashanth19975/prashanth19975.git'
        // Get the Maven tool.
        // ** NOTE: This 'M3' Maven tool must be configured
        // **       in the global configuration.
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
    stage('mvn deploy') {
        // Run the maven build
        sh 'mvn deploy'
     }
}
