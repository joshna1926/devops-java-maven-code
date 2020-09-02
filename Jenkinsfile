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
		stage('build'){
                   agent any {
                docker {
                image 'maven'
                args '-v $HOME/.m2:/root/.m2'
                }
            }
                   steps{
                      script{
                        sh 'mvn -B -DskipTests clean package'
                       }
                    }
              }
        }
}
                    

