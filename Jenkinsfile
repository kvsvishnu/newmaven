node('master') 
{
    stage('ContinuousDownload_loans')
    {
        git 'https://github.com/kvsvishnu/maven.git'             
    }
    stage('ContinuousBuild_loans')
    {
        sh 'mvn package'
    }
}
