pipeline {
    agent any 
    stages {
        stage('Compile') { 
            steps { 
   		withMaven(maven : 'maven_3_6_0'){
		sh 'mvn clean install'
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test'
                junit 'reports/**/*.xml' 
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
	stage('Package') {
            steps {
                sh 'mvn install'
            }
        }
    }
}
