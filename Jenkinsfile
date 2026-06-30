pipeline {
   agent any

   stages {

       stage('Clean') {
           steps {
               sh 'mvn clean'
           }
       }

       stage('Test') {
           steps {
               
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
