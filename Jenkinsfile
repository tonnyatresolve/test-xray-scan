pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK15'
    }

    stages {
        stage('Git clone') {
            steps {
                git url: 'https://github.com/tonnyatresolve/test-frog-notification.git'
            }
        }
        stage('Build code') {
            steps {
                withMaven (
                    maven: 'Maven'
                ) {
                    sh "mvn deploy"
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}