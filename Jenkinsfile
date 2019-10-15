pipeline {
    agent any
    stages {
 
       stage ('Compile Stage') {
         withMaven (Maven : 'Maven_3_5_0') {
             sh 'mvn clean compile'
         }
         stage ('Testing Stage') {
          withMaven (Maven : 'Maven_3_5_0') {
             sh 'mvn test'
         }

         stage ('Deploy Stage') {
          withMaven (Maven : 'Maven_3_5_0') {
             sh 'mvn deploy'

       }
            
            }
      
      }
       }
    }
