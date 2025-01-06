#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm start'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm start'
            }
        }
    }
}
