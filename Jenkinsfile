pipeline{
           agent {
              label 'harshal-agent-1'          
           }
        stages {
            stage("checkout the code"){
                steps{
                    checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/HarshalYeola20/javademo.git']])
                }
            }
            stage("build the job"){
                steps{
                    sh 'mvn package'
                }
            }
        }
        post{
            always{
               cleanWs() 
            }
        }
            
}
