pipeline {
   agent any
       stages {
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
          stage('Deploy') {
            steps {
                "cp -R C:/Users/Lenovo/.jenkins/workspace/pipelinetomcat/target/* C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps"
            }
          }
          
    }
}
