pipeline{
    agent any
    environment{
        PATH= "/usr/share/maven/bin:$PATH"
    }
    stages{
        stage('Git Checkout.'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/abhikandula/webhook-test.git']]])    
            }
        }
        stage('Maven Build.'){
            steps{
            sh "maven clean package"    
                
            }
        }
        
    }
}
