pipeline{
	
	agent any

	stages{
	stage ('Packag Stage'){
		steps {
		withMaven(maven : 'maven_3_6_0'){
		sh 'mvn clean package'

				}
			}
		}
	}

}
