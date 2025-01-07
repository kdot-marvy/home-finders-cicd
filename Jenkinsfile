#!/usr/bin/env groovy

pipeline {

    agent any
    stages {
        stage('Test') {
            steps {
                sh '''
                    node --version
                    docker ps
                '''
            }
        }
        stage('Prune Docker data') {
            steps {
                sh 'docker system prune -a --volumes -f'
            }
        }
        stage('Start containers') {
            steps {
                sh 'docker compose up -d --no-color --wait'
                sh 'docker compose ps'
            }
        }
    }
}
