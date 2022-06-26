pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ThanhNguyen281297/Web-WP.git'
            }
        }
        stage('Install Web Server Nginx') {
            steps {
                sh 'apt install nginx -y'
                sh 'systemctl status nginx'
            }
        }
    }
}