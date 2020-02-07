pipeline {
   agent  {
       kubernetes {
          containerTemplate {
            name 'maven'
            image 'maven:3.3.9-jdk-8-alpine'
            ttyEnabled true
            command 'cat'
          }
       }
   }
   stages {
      stage('Build') {
         steps {
            echo 'Hello World'
         }
      }
       
      stage('Test') {
         parallel {
            stage('Chrome'){
               steps{
                  sh 'echo "Chrome"'
               }
            }
            stage('Firefox'){
               steps {
                  sh 'echo "Firefox"'
               }
            }
         }
         
      }
      
   }
}
