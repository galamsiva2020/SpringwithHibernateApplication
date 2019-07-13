node{
  def mvnHome 
  def scannerHome
stage('SCM Checkout'){

 git 'https://github.com/galamsiva2020/SpringwithHibernateApplication.git'
 }
 
 stage('MavenHome'){
          mvnHome ='D:/GALAM/SivaDevopsSoftwares/apache-maven-3.6.0-bin/apache-maven-3.6.0'
       // sh "${mvnHome}/bin/mvn package"
}

  stage('SonarQube analysis') {
     scannerHome = 'C:/Users/Vamsi/Downloads/sonarqube-7.2.1/sonarqube-7.2.1'
    withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
  }
