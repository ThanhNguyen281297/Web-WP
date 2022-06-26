pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ThanhNguyen281297/Web-WP.git'
            }
        }
        stage('Copy source to Web Server') {
            steps {
                sh 'cp -r /var/lib/jenkins/workspace/\r'Build Web WP Pipeline' /var/www/html'
                sh 'echo Done copy source'
                sh 'rm -rf /var/www/html/index-nginx-debian.html'
                sh 'Done remove defaut nginx page'
            }
        }
    }
}