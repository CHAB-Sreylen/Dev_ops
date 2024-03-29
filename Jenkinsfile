pipeline {
    agent any // window agent, Jenkins-laravel (other machine)
    environment {
        BOT_TOKEN = "6631869120:AAHaUSsakEu_xiB76WTZJPxSWvJXNo_ZjRs"
        CHAT_ID = "-1001996412138"
    }
    stages {
        stage('Fetch from GitHub') { //build steps
            steps {
                echo 'Fetching for GitHub'
                git branch: 'main', url: 'https://github.com/CHAB-Sreylen/Dev_ops.git'
            }
        }
        stage('Hello'){
            steps{
                echo'Hello Welcome'
            }
        } 
    }
    post{
            success{
                sh '''
                sh 1-success-deploy.sh;\
                '''
            }
            failure{
                sh '''
                sh 2-fail-deploy.sh;\
                '''
            }
    }

}
    