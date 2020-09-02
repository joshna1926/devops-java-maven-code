def getDockerTag(){
        def tag = sh script: 'git rev-parse HEAD', returnStdout: true
        return tag
}
pipeline {
    agent {
        docker { image 'maven' }
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean package '
            }
        }
    }
}
                    

