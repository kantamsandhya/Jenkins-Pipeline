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
                sh "cp -R C:\Users\Lenovo\Downloads\apache-tomcat-9.0.41\bin C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps"
            }
        }       
    }
}
