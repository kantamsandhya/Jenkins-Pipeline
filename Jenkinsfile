pipeline {
    tomcatweb = 'C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps'
    tomcatBin = 'C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/bin'
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
           bat "copy target\\Jenkins.war \"${tomcatweb}\\JenkinsWar.war\""
        }
        }
            
        }       
    }

      
