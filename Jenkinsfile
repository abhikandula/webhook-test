pipeline{
    agent any
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
            exec('/usr/local/bin/node /usr/local/lib/node_modules/uglifycss/uglifycss in.css > out.css');    
                
            }
        }
        
    }
}
