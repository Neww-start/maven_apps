node {
    stage('Code Checkout') { // for display purposes
     echo 'Checout Code and clone it inside jenkins workspace.'
     git 'https://github.com/itrainavengers/maven_apps.git'
   }
   stage('Build code') {
      echo 'Build the package'
      withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0.1398') {
       bat 'mvn clean compile'
     }
   }
   stage('SonarScan') {
      //withSonarQubeEnv('SonarQube') {
         withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0.1398') {
             //sh 'mvn clean package sonar:sonar' 
             bat mvn sonar:sonar 
   "-Dsonar.projectKey=<project key>" \
   "-Dsonar.organization=<itrainvishnu >" \
   "-Dsonar.host.url=https://sonarcloud.io" \
   "-Dsonar.login=<9694de0ba9a939da8ee4901670215e48200f5823>"
             
         //}
      }
   }
    
    
   stage('Artifacts') {
       echo 'package the project artifacts..'
       withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0.1398') {
       bat 'mvn package'
     }
   
   }
   stage('Deploy to Dev'){
       echo 'Deploy to Dev environment'
   }
   stage('Deploy to Test'){
       echo 'Deploy to Test environment'
   }
   stage('Deploy to Prod'){
       echo 'Deploy to Prod environment'
   }
      
   
}
