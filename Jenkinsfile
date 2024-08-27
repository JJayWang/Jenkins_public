// @Library('sharedlibrary.jjay.deployment@main') _
library 'sharedlibrary.jjay.deployment@main'

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
                    pwd
                }
            }
        }
    }
}

def FileInnerFunction() {
    echo "this is inner function!"
}
