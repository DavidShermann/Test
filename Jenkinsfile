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
                sh 'git merge feature main'
            }
        }
    }
}
