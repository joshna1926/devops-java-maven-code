pipeline {
 agent none

 stages
 {
  agent { label 'none' }
  stage('Checkout')
  {
   steps { 
    git branch: 'master', url: 'https://github.com/mudipallinarasimhulu/devops-java-maven-code.git'
   }
  }
 }
}
