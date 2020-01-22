pipeline{
    agent any
    stages{
        stage('Git Checkout.'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/abhikandula/webhook-test.git']]])    
            }
        }
        
    }
}
