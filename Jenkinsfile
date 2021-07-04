node('master') 
{
    stage('ContinuousDeployment_loans')
    {
sh 'scp /home/ubuntu/.jenkins/workspace/MultiP_master/webapp/target/webapp.war ubuntu@172.31.33.103:/var/lib/tomcat8/webapps/testapp.war'
    }

    stage('ContinuousTesting_loans')
    {
        git 'https://github.com/kvsvishnu/FunctionalTesting.git'
        sh 'java -jar /home/ubuntu/.jenkins/workspace/MultiP/testing.jar'
    }
    stage('ContinuousDelivery_loans')
    {
    
    sh 'scp /home/ubuntu/.jenkins/workspace/MultiP_master/webapp/target/webapp.war ubuntu@172.31.42.175:/var/lib/tomcat9/webapps/prodapp.war'}
}
