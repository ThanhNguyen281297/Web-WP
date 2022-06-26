pipeline {
    agent any
    stages {
        stage('Clone code') {
            steps {
                git 'https://github.com/ThanhNguyen281297/Web-WP.git'
                sh 'echo Done clone code' 
            }
        }
        stage('Build'){
            steps {
                sh "scp -r '/var/lib/jenkins/workspace/Pipeline' root@192.168.26.108:/var/www/html"
            }
        }
        stage('Deploy'){
            steps {
                sh 'ssh root@192.168.26.108'
                sh "sed -i 's/root /var/www/html;/root /var/www/html/Pipeline;/g /etc/nginx/sites-available/default"
                sh 'cat /etc/nginx/sites-available/default'
            }
        }
    }
}