pipeline{
    agent any
        }
    tools{
    maven 'maven 3'
    jdk 'java 8'
         }
    stages{
        stage('Git Checkout.'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/abhikandula/webhook-test.git']]])    
            }
        }
        stage ("initialize") {
            steps {
            sh '''
            echo "PATH = ${PATH}"
            echo "M2_HOME = ${M2_HOME}"
            '''
          }
        }   
                                   
            }
        }
        
    }
}
