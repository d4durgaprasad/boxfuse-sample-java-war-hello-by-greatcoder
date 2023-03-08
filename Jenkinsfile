pipeline
{
 agent any
 environment {
       PATH = "/bin/mvn:$PATH"
   }
   
   
   stages {
       stage("get the code from git"){
           steps{
              git branch: 'master', url: 'https//github.com/Rajakokk/boxfuse-sample-java-war-hello.git'

             }
          }





 stage("build the code")
       {
              steps{
                  sh "mvn clean package"
               }
       }


          stage("deploy the code")
                {
              steps{
                deploy adapters: [tomcat9(credentialsId: 'DEPLOYY', path: '', url: 'http://http://100.26.226.134:8080//')], contextPath: 'myapplication', war: '**/*.war'
               }
           }
       
  }




    

