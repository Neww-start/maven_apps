node {
   
   stage('Code Checkout') { 
     git credentialsId: 'githubID', url: 'https://github.com/itrainbatman/maven_apps.git' 
    }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn test'
      } 
    }
    }
   
   stage('Deploy to Dev') {
     
    }
   stage('Automation Testing') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Smoke Testing') {
     
    }
   stage('Deploy to Prod') {
     
    }
   stage('Acceptance Testing') {
     
    }
