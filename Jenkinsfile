#!/usr/bin.env groovy

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
                    def dockerCmd = 'docker run -p 3090:3000 -d cnwagba/jenkins-repo-dockerhub:1.0.4-28'
                    sshagent(['ec2-key-27']) {
                        sh "ssh -o StrictHostKeyChecking=no ec2-user@44.193.200.99 ${dockerCmd}"
                    }
                }
            }
        }               
    }
} 
