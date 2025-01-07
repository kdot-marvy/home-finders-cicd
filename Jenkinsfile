#!/usr/bin/env groovy

pipeline {

    agent { dockerfile true }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Build Image') {
            steps {
                echo 'Building Docker Image...'
                sh 'docker ps'
                sh 'docker build -t my-node-app:1.0.0 .'
            }
        }
    }
}
