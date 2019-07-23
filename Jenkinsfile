node{
 
stage('SCM Checkout'){

 git 'https://github.com/galamsiva2020/SpringwithHibernateApplication.git'
 }
 
 stage('MavenHome'){
          mvnHome ='C:/Program Files (x86)/apache-maven-3.6.0-bin/apache-maven-3.6.0'
      
}
 
 /* stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 6.2';
    withSonarQubeEnv('LocalSonarQubeserver') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }*/
/* 
stage('SonarQube analysis') {
    withSonarQubeEnv('LocalSonarQubeserver') {
      sh 'mvn clean package sonar:sonar'
     // submitted SonarQube taskId is automatically attached to the pipeline context
  }
} 
*/
 
 stage('SonarQube analysis') {
  scannerHome= 'D:/GALAM/sonarqube-6.2/sonarqube-6.2/bin/windows-x86-64'
    //ws('D:\\my_prj') {
    // requires SonarQube Scanner 2.8+
   // def scannerHome = tool 'sonarScanner';
    //withSonarQubeEnv('SonarQube 6.2') {
      //bat "${scannerHome}/bin/sonar-scanner.bat"
   //}
  }
}
 
  }
