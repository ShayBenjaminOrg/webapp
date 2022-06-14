pipeline {
    agent any 
    stages {
        stage('Clone the repo') {
            steps {
                sh 'whoami'
                echo 'clone the repo'
                sh 'rm -fr html'
                sh 'git clone https://github.com/shaybenjamin/webapp1.git'
            }
        }
        stage('push repo to remote host') {
            steps {
                echo 'connect to remote host and pull down the latest version'
                sh 'ssh -i ~/.ssh/mtckey ec2-user@10.0.1.139 sudo git -C /var/www/html pull'
            }
        }
        stage('Check website is up') {
            steps {
                echo 'Check website is up'
                sh 'curl -Is 10.0.1.139 | head -n 1'
            }
        }
    }
}
