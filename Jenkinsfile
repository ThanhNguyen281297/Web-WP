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
                sh 'systemctl status nginx'
                sh 'systemctl enable nginx'
                sh 'echo Done Install Nginx'
            }
        }
        stage('Install MySql'){
            steps {
                sh 'sudo apt install mysql-server'
                sh 'systemctl status mysql'
                sh 'systemctl enable mysql'
                sh 'echo Done Install Mysql'
            }
        }
        stage('Setup Mysql') {
            steps {
                sh 'sudo mysql -u root -p'
                sh 'CREATE DATABASE WordPress CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;'
            }      
        }
    }
}