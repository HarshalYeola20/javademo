pipeline{
           agent {
              label 'harshal-agent-1'          
           }
           parameters {string defaultValue: 'master' , name: 'branch_name'}
        stages {
            stage("checkout the code"){
                steps{
                     git branch: "$branch_name", url: 'https://github.com/HarshalYeola20/javademo.git'       
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
