pipeline {
    agent any
    stages {
        stage('SSH to Web server') {
            steps {
                sh 'ssh root@192.168.26.108'
                sh '-----------------------'
                sh 'echo Done SSH'
                sh '-----------------------'
            }
        }
        stage('Update and upgrade package') {
            steps {
                sh 'apt update && apt upgrade -y'
                sh '-----------------------'
                sh 'echo Done Update and Upgrade'
                sh '-----------------------'
            }
        }
        stage('Install Web Server Nginx') {
            steps {
                sh 'apt install nginx'
                sh 'systemctl status nginx'
                sh 'systemctl enable nginx'
                sh '-----------------------'
                sh 'echo Done Install Nginx'
                sh '-----------------------'
            }
        }
        stage(''){
            steps {
                sh 'apt install mysql-server'
                sh 'systemctl status mysql'
                sh 'systemctl enable mysql'
                sh '-----------------------'
                sh 'echo Done Install Mysql'
                sh '-----------------------'
            }
        }
    }
}