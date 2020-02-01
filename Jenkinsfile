pipeline {

    agent any
    tools {
        maven 'mvn' 
    }
    stages {
        stage('Compile stage') {
            steps {
                sh "mvn clean install" 
        }
    }

         stage('testing stage') {
             steps {
                sh "mvn test"
        }
    }

        stage('Deploy') {
            steps {
                sh "scp -r /root/.jenkins/workspace/Decl-PipeLine/in28minutes-web-servlet-jsp/target/*.war root@172.18.97.43:/opt/apache-tomcat-7.0.94/webapps/"
            }
        }

  }

}
