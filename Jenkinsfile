pipeline {
   def tomcatweb = 'C:\Users\Lenovo\Downloads\apache-tomcat-9.0.41\webapps'
   def tomcatBin = 'C:\Users\Lenovo\Downloads\apache-tomcat-9.0.41\bin'
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
            steps {
               bat "${tomcatBin}\\startup.bat"
            }
        }       
    }
}
      
