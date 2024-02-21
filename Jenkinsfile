pipeline {
    agent any
    stages {
        stage('test1') {
            steps {
	        sh 'python3 -m pytest test.py'
            }
        }
        stage('Push to master') {
            steps{
                withCredentials([gitUsernamePassword(credentialsId: 'TEST', gitToolName: 'Default')]) {
                    sh "git push -u feature main"
            }
        }
    }
}
}