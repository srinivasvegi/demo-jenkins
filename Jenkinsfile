pipeline {
    agent any
    stages {
        stage ('SCM Commit'){
        git 'https://github.com/srinivasvegi/demo-jenkins/blob/master/Jenkinsfile'
        }
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
