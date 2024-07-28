#!/usr/bin.env groovy

library identifier: 'Jenkins-shared-lib@main', retriever: modernSCM(
    [$class: 'GitSCMSource',
    remote: 'https://github.com/nenye18/Jenkins-shared-lib.git',
    credentialsID: 'GitHub credentials'
    ]
)

pipeline {   
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "Testing the application..."

                }
            }
        }
        stage("build") {
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    echo "Deploying the application..."        
                }
            }
        }               
    }
} 
