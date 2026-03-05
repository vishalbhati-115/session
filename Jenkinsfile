pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/vishalbhati-115/session.git'
    
            }
       }
         stage('Build') {
            steps {
                bat 'javac demo.java'
    
            }
       }
         stage('Execute') {
            steps {
                bat 'java demo'
    
            }
       }
       
    }
}
