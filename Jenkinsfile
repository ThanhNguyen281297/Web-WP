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
                sh 'apt update && apt upgrade -y'
                sh 'echo Done Update and Upgrade'
            }
        }
        stage('Install Web Server Nginx') {
            steps {
                sh 'apt install nginx'
                sh 'systemctl status nginx'
                sh 'systemctl enable nginx'
                sh 'echo Done Install Nginx'
            }
        }
        stage('Install MySql'){
            steps {
                sh 'apt install mysql-server'
                sh 'systemctl status mysql'
                sh 'systemctl enable mysql'
                sh 'echo Done Install Mysql'
            }
        }
    }
}