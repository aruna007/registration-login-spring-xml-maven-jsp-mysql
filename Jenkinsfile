node
    {
     stage ('scm checkout')
     {
      git 'https://github.com/aruna007/registration-login-spring-xml-maven-jsp-mysql'
     }
     stage('mvn compile')
     {
         def mvnHome = tool name: 'maven', type: 'maven'
         def mvnCMD = "${mvnHome}"
         sh "${mvnCMD} clean compile"
        }
        stage('mvn test')
     {
         def mvnHome = tool name: 'maven', type: 'maven'
         def mvnCMD = "${mvnHome}"
         sh "${mvnCMD} test"
        }
        stage('mvn package')
     {
         def mvnHome = tool name: 'maven', type: 'maven'
         def mvnCMD = "${mvnHome}"
         sh "${mvnCMD} package"
        }
        stage ('deploy')
        {
         sh "sudo cp /var/lib/jenkins/workspace/groovy_test/target/account-1.0-SNAPSHOT.war /root/arun/apache-tomcat-9.0.22/webapps"
        }
        
     }
