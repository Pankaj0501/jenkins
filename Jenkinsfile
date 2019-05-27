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
                withMaven(maven : 'MAVEN_PIPELINE')
                {
                    sh 'mvn clean install'
                }
            }
        } 
    }
}
