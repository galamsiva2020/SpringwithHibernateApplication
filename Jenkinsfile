node{
 
stage('SCM Checkout'){

 git 'https://github.com/galamsiva2020/SpringwithHibernateApplication.git'
 }
 
 stage('MavenHome'){
          mvnHome ='D:/GALAM/SivaDevopsSoftwares/apache-maven-3.6.0-bin/apache-maven-3.6.0'
      
}

 stage('SonarQube analysis') {
    withSonarQubeEnv(credentialsId: '5573752016db3b4ea336341bdfb80fc51f0d0f93', installationName: 'SonarServer') { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
    }
  }
 
 /* stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }*/
  
  }
