pipeline {
  agent any
  stages {
    stage('Source') { // Get code
      steps {
        // get code from our Git repository
        git 'https://github.com/brentlaster/roarv2'
      }
    }
    stage('Compile') { // Compile and do unit testing
	withMaven(maven : 'maven_3_6_0'){
		sh 'mvn clean compile'
	}
    }
  }
}
