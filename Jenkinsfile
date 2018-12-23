pipeline{
	
	agent any

	stages{
		stage ('Compile Stage'){

			steps {

			withMaven(maven : 'maven_3_5_2'){
				sh 'mvn clean compile'

			}
		}
	}

		stage ('Testing Stage'){

			steps {

			withMaven(maven : 'maven_3_6_0'){
				sh 'mvn test'

			}
		}
	}
		stage ('Packag Stage'){

			steps {

			withMaven(maven : 'maven_3_6_0'){
				sh 'mvn clean package'

			}
		}
	}

	}
}
