pipeline
{
    agent any
    tools {
        maven 'MVN' 
    }
    stages
    {
        stage('Compile Stage')
        {
            steps
            {
                    sh "mvn clean install"
            }
        }
        
        stage('testing stage')
        {
            steps 
            {
                sh "mvn test"
            }
       }

        stage('Deploy')
        {
            steps 
            {
                sh "scp -r /home/heena/.jenkins/workspace/pipelineJob/in28minutes-web-servlet-jsp/target/*.war kaira@172.31.12.210:/home/kaira/apache-tomcat-8.5.41/webapps            }
        }
    }
}
