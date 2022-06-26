pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo SSH to Web Server'
                sh 'ssh root@192.168.26.108'
                sh 'echo Done SSH'
                sh 'echo Update and upgrade package'
                sh 'sudo apt update -y '
                sh 'sudo apt upgrade -y'
                sh 'echo Done Update and Upgrade'
                sh 'Install Web Server Nginx'
                sh 'sudo apt install nginx'
                sh 'sudo systemctl status nginx'
                sh 'sudo systemctl enable nginx'
                sh 'echo Done Install Nginx'
            }
        }
    }
}