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
                sh "cp -r /var/lib/jenkins/workspace/'Build Web WP Pipeline' /var/www"
                sh 'echo Done copy source'
                sh "mv /var/www/'Build Web WP Pipeline' /var/www/WebWP"
                sh 'echo Done rename'
            }
        }
    }
}