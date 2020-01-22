pipeline{
    agent any
        }
    envirnoment{
    PATH=" /usr/share/maven/bin:$PATH"    
    }
    stages{
        stage('Git Checkout.'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/abhikandula/webhook-test.git']]])    
            }
        }
        stage ("Maven Build"){
            Steps{
            sh " mvn clean package"
            }
        }   
                                   
            }
        }
        
    }
}
