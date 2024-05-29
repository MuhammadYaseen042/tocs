pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building App...'
                sh  'node --version'
            }
        }
        stage('Deploying') {
            steps {
                echo 'Deploying App...'
                sh 'node App.js'
                sh 'gcloud compute zones list'
                sh 'gcloud compute scp /var/lib/jenkins/workspace/Test_main/index.html root@apache-server:/var/www/html --zone=us-west4-b'
            }
}
}
}

