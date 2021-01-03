pipeline {
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
                bat "copy C:/Users/Lenovo/.jenkins/workspace/Jenkins_Pipeline/target/* C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps"
            }
        }       
    }
}
      
