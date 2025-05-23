pipeline {
    agent any 

    stages { 

        stage('Run Docker Image') {
            steps {
               script {
                     docker.build("hello-devops")
                   }
               }      
           }
         

         stage('Run Docker Container') {
              steps {
                  sh "docker run -d -p 8081:80 hello-devops"
               }
            }
         }
     }
