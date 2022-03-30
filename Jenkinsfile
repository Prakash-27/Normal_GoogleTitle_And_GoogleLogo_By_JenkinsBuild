pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build app'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test app'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy app'
            }
        }
    }
    post{
        always{
            build 'Build'
            emailext body: '''Summary 
            Here Build FreeStyle Project is used''', subject: 'Pipeline Status', to: 'shanmugabhuvanesh2603@gmail.com'
        }
    }
}
