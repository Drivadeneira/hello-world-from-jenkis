pipeline {
    agent any

    tools {
        nodejs 'NodeJS 18' // 👈 this name must match what you set
    }

    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'nohup npm start &'
            }
        }

        stage('Show App Info') {
            steps {
                echo 'This is your app! Access it at: http://localhost:3000'
            }
        }
    }
}