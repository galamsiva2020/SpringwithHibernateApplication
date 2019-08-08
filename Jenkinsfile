// Powered by Infostretch 

timestamps {

node () {

	stage ('SpringApplication-AWSTest - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a03b1ab3-f4d2-44a5-b98f-040b8fe3d562', url: 'https://github.com/galamsiva2020/SpringwithHibernateApplication.git']]]) 
	}
	stage ('SpringApplication-AWSTest - Build') {
 	
withEnv(["JAVA_HOME=${ tool '"+JDK+"' }", "PATH=${env.JAVA_HOME}/bin"]) { 
		// Maven build step
	withMaven(jdk: '(Inherit From Job)', maven: 'MyMaven') { 
 			if(isUnix()) {
 				sh "mvn package " 
			} else { 
 				bat "mvn package " 
			} 
 		}
// Unable to convert a build step referring to "hudson.plugins.sonar.SonarRunnerBuilder". Please verify and convert manually if required. 
	}
}
}
}