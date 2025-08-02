pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repo...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                echo 'Running the app on port 8087...'
                sh 'nohup npm start &'
            }
        }
    }
}