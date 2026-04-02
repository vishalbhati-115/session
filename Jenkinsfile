pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               git 'https://github.com/vishalbhati-115/session.git',branch: 'master'
            }
        }
         stage('Build Image') {
            steps {
            bat 'docker build -t mywebsite .'
            }
        }
    
    stages('Stop old Container'){
        steps{
            bat 'docker stop mycont || exit 0'
            bat 'docker rm mycont || exit 0'
        }
    }
    stages('Run Image - Containerize'){
        steps{
            bat 'docker run -d -p 7000:80 --name mycont mywebsite'
           
        }
    }
        
    }
}
