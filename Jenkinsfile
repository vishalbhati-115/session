pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               git 'https://github.com/vishalbhati-115/session.git'
            }
        }
         stage('publish') {
            steps {
            publishHTML([
                allowmissing:true,
                alwaysLinktoLastBuild:false,
                keepAll:false,
                reportDir:'.',
                reportFiles:hello.html
                report:MY FIRST
                ])
            }
        }
    }
}
