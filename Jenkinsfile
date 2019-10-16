pipeline {
    agent any
    stages {
        stage ('SCM Commit'){
        git 'https://github.com/srinivasvegi/demo-jenkins/blob/master/Jenkinsfile'
        }
       stage ('Compile Stage') {
         withMaven (Maven : 'Maven_3_5_0') {
             sh 'mvn --version'
         }
         stage ('Testing Stage') {
          withMaven (Maven : 'Maven_3_5_0') {
             sh 'echo "my forst code"'
         }
            
        }
      
      }
    }
}
