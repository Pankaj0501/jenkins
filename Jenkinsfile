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
                    sh 'mvn clean compile'
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
            sh label: '', script: 'scp -r $WORKSPACE/in28minutes-web-servlet-jsp/target/*.war heena@172.31.16.151:/home/heena/apache-tomcat-7.0.94/webapps'
        }
        
    }
}
