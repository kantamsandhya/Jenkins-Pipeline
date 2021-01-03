pipeline {
   def tomcatweb = 'C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps'
   def tomcatBin = 'C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/bin'
   def tomcatStatus = ''
   agent any
       stages {
        stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') {
           bat "copy target\\Jenkins.war \"${tomcatweb}\\JenkinsWar.war\""
        }
            stage('Start Tomcat Server') {
               sleep(time:5,unit:"SECONDS")
               bat "${tomcatBin}\\startup.bat"
               sleep(time:100,unit:"SECONDS")
            }
        }       
    }
}
      
