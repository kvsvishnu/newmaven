node('master') 
{
    stage('ContinuousDeployment_loans')
    {
sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.23.20:/var/lib/tomcat9/webapps/testapp.war'
    }

    stage('ContinuousTesting_loans')
    {
        git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
        sh 'java -jar /home/ubuntu/.jenkins/workspace/ScriptedPipeline/testing.jar'
    }
    stage('ContinuousDelivery_loans')
    {
    
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.28.60:/var/lib/tomcat9/webapps/prodapp.war'}
}
