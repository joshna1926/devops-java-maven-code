
pipeline {
 agent none

 stages
 {
  agent { label 'any' }
  stage('Checkout')
  {
   steps { 
    git branch: 'master', url: 'https://github.com/mudipallinarasimhulu/devops-java-maven-code.git'
   }
  }

  stage('Build War')
  {
   agent { label 'any' }
   steps { 
    sh "mvn clean package"
   }
  }
