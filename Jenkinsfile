pipeline {
    agent any
    environment{
        DOCKER_IMAGE = 'node-api'
    }

    stages {
        stage('Checkout') {
            steps {
                // Replace with your GitHub repo
                git branch: 'main', url:'https://github.com/Saeshu/devops'
            }
        }

        stage('Install Dependencies') {
            steps {
                
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                
                bat 'echo no tests yet'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %DOCKER_IMAGE% , '
            }
        
        }
        stage('Run Container'){
            stpes{
                bat 'docker run -d -p 3000:3000 %DOKCER_IMAGE%'
                }
            }
        }
    }
        
   