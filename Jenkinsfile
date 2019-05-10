pipeline
{
    agent any
    stages
    {
        stage('Compile Stage')
        {
            steps
            {
                withMaven(maven : 'MAVEN_PIPELINE')
                {
                    sh 'mvn clean install
                }
            }
        }
        stage('Testing Stage')
        {
            steps
            {
                withMaven(maven : 'MAVEN_PIPELINE')
                {
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy')
        {
            steps
            {
               sh 'scp -r /home/heena/.jenkins/workspace/pipelineJob/in28minutes-web-servlet-jsp/target/*.war heena@172.31.16.151:/home/heena/apache-tomcat-7.0.94/webapps'
            }    
        }
        
    }
}
