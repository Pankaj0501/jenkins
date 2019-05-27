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
    }
}
