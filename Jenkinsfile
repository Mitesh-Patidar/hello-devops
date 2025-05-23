pipeline {
    agent any 

    stages {
        stage('Clone Repo') {
            steps {
                 git 'https://github.com/Mitesh-Patidar/hello-devops.git'
            } 
        } 

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
