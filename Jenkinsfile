pipeline {
    agent any
    stages {
        stage('SSH to Web server') {
            steps {
                sh 'ssh root@192.168.26.108'
                sh 'echo Done SSH'
            }
        }
        stage('Update and upgrade package') {
            steps {
                sh 'sudo apt update -y '
                sh 'sudo apt upgrade -y'
                sh 'echo Done Update and Upgrade'
            }
        }
        stage('Install Web Server Nginx') {
            steps {
                sh 'sudo apt install nginx'
                sh 'sudo systemctl status nginx'
                sh 'sudo systemctl enable nginx'
                sh 'echo Done Install Nginx'
            }
        } 
    }
}