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
                    def dockerCMD = 'docker run -p 3000:3000 -d cnwagba/jenkins-repo-dockerhub:1.0.1'
                    sshagent(['ec2-key']) {
                        sh "ssh -o StrictHostKeyChecking=no ec2-user@54.174.84.169 ${dockerCmd}"
                    }
                }
            }
        }               
    }
} 
