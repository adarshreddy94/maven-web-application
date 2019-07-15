// Powered by Infostretch 

timestamps {

node () {

	stage ('flipkart-dev - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Adarshreddy94', url: 'https://github.com/adarshreddy94/maven-web-application.git']]]) 
	}
	stage ('flipkart-dev - Build') {
 			// Maven build step
	withMaven(maven: 'Maven 3.6.1') { 
 			if(isUnix()) {
 				sh "mvn clean
package " 
			} else { 
 				bat "mvn clean
package " 
			} 
 		} 
	}
}
}