node{
   
   def tomcatweb = 'C:\Users\Lenovo\Downloads\apache-tomcat-9.0.41\webapps'
   def tomcatBin = 'C:\Users\Lenovo\Downloads\apache-tomcat-9.0.41\bin'
   def tomcatStatus = ''
   stage('SCM Checkout'){
      git 'https://github.com/kantamsandhya/Jenkins-Pipeline.git'
   }
   stage('Compile-package-create-war-file'){
      //get maven home path
      def mvnHome = toolname: 'maven-3.6.3', type: 'maven'
      bat "${mvnHome}/bin/mvn package"
   }
   stage('Deploy to tomcat'){
      bat "copy target\\jenkins.war \"${tomcatweb}\jenkinswar.war\""
   }
   stage ('Start Tomcat Server') {
      sleep(time:5,unit:"Seconds")
      bat "${tomcatBin}\\Startup.bat"
      sleep(time:100,unit:"SECONDS")
   }
}

      
