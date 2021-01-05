node {
   stage('Git Repo'){
    git url: 'https://github.com/kantamsandhya/Jenkins-Pipeline.git', branch: 'master'
}
       
        stage("Maven Build") {
            def mavenHome = tool name: "maven3.6.3", type: "maven"
           bat "${mavenHome}/bin/mvn clean package"
        }
   stage("Deploy to tomcat")
        {
        "cp  C:/Users/Lenovo/.jenkins/workspace/Tomcat/target/binary/* C:/Users/Lenovo/Downloads/apache-tomcat-9.0.41/webapps/"
        }
}
