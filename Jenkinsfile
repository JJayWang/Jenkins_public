@Library('sharedlibrary.jjay.deployment@main') _
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // 調用 Shared Library 中的方法
                    mySharedFunction()
                }
            }
        }
        stage('Build 2') {
            steps {
                script {
                    echo "jenkins from github"
                }
            }
        }
        stage('Call Inner Function') {
            steps {
                script {
                    FileInnerFunction()
                }
            }
        }
    }
}

def FileInnerFunction() {
    echo "this is inner function!"
}
