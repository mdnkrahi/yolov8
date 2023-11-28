pipeline {
    agent {
        node {
            label 'slave'
			docker { image 'node:7-alpine' }
        }
    }
	
    stages {
        stage('clone') {
            steps {
                sh 'pwd'
            }
        }
    }
}