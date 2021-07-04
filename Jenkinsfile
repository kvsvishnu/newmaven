node('master') 
{
    stage('ContinuousDownload_master')
    {
        git 'https://github.com/kvsvishnu/maven.git'             
    }
    stage('ContinuousBuild_master')
    {
        sh 'mvn package'
    }
}
