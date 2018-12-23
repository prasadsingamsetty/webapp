pipeline{
	
	agent any

	stages{
	stage ('Packag Stage'){
		steps {

		withMaven(maven : 'maven_3_6_0'){
		sh 'mvn clean install'

			}
		}
	stage('Deploy') {
            	steps {
                sudo cp target/*.war /opt/tomcat/webapps
            }
        }
	
}

}
