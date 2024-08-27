// @Library('sharedlibrary.jjay.deployment@main') _
library 'sharedlibrary.jjay.deployment@main'

pipeline {
    agent any
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
        FOLDER_NAME  = 'JJFolder'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    // 調用 Shared Library 中的方法
                    // mySharedFunction()
                    echo "${FOLDER_NAME}"
                    sh """
                        mkdir ${FOLDER_NAME}
                        cd ${FOLDER_NAME}
                        echo pwd
                    """
                    // echo "This is ${FOLDER_NAME}"
                    // sh 'printenv'
                }
            }
        }
        // stage('Build 2') {
        //     steps {
        //         script {
        //             echo "jenkins from github"
        //             parallel (
        //                 "p1": {
        //                     sh "echo this is p1"
        //                 },
        //                 "p2": {
        //                     sh "echo this is p2"
        //                 }
        //             );
        //         }
        //     }
        // }
        // stage('Call Inner Function') {
        //     steps {
        //         script {
        //             FileInnerFunction()
        //             sh """ pwd """
        //         }
        //     }
        // }
    }
}

def FileInnerFunction() {
    echo "this is inner function!"
}
