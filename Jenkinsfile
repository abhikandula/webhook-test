node
{
   stage('checkout')
   {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-credential', url: 'https://github.com/abhikandula/webhook-test.git']]])   
   }
   stage('static code analysis')
   {
    echo 'static code analysis'   
   }
   stage('build stage')
   {
    echo 'build pipeline'
   }   
}
