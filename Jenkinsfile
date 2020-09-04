 def getDockerTag(){
       def tag = sh script: 'git rev-parse HEAD', returnStdout: true
        return tag
        }
        
  pipeline{
        agent any  
        environment{
	    Docker_tag = getDockerTag()
        }
        
        stages{
		
        stage('Build War')
  {
  
   steps { 
    sh "mvn clean package"
   }
  }
	}
  }
  
