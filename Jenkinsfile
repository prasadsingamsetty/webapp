pipeline {
    agent any 
    stages {
        stage('Compile') { 
            steps { 
   		withMaven(maven : 'maven_3_6_0'){
		sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
	stage('Install') {
            steps {
                sh 'mvn install'
            }
        }
    }
}
}
