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
                allowMissing:true,
                alwaysLinkToLastBuild:false,
                keepAll:false,
                reportDir:'.',
                reportFiles:"hello.html",
                reportName:"MY HELLO WORLD"
                ])
            }
        }
    }
}
