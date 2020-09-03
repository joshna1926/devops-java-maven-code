
pipeline {
 agent any

 stages
 {
   stage('Checkout')
  {
   steps { 
    git branch: 'master', url: 'https://github.com/mudipallinarasimhulu/devops-java-maven-code.git'
   }
  }

  stage('Build War')
  {
  
   steps { 
    sh "mvn clean package"
   }
  }
 }
}
