pipeline
{
    agent any
    tools {
        maven 'MVN_3.6.1' 
    }
    stages
    {
        stage('Compile Stage')
        {
            steps
            {
                withMaven(maven : 'MAVEN_PIPELINE')
                {
                    sh 'mvn clean install'
                }
            }
        } 
    }
}
