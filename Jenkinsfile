pipeline {
    agent any

    stages {
        stage('pull code') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '97cdbcb4-8185-4a05-9fb3-6f5a46066e40', url: 'git@github.com:beichenyibei/demo.git']]])
            }
        }
        stage('package code') {
            steps {
                sh 'mvn clean package'
            }
        }

    }
}
