pipeline {
   agent any

   tools {
       jdk 'JDK21'
       maven 'Maven3'
   }

   stages {

       stage('Clean') {
           steps {
               sh 'mvn clean'
           }
       }

       stage('Test') {
           steps {
               sh 'mvn test'
           }
       }

       stage('Package') {
           steps {
               sh 'mvn package'
           }
       }
   }

   post {
       success {
           archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
       }
   }
}
