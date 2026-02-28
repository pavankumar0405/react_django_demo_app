pipeline {
    agent any 
    stages{
        stage('Code'){
            steps{
                git url: 'https://github.com/pavankumar0405/react_django_demo_app.git', branch: 'main'
            }
        }
        stage('Build'){
            steps{
                sh 'docker build . -t todo-app-test:latest'
            }
        }
        stage('Test'){
            steps{
                git url: 'https://github.com/pavankumar0405/react_django_demo_app.git', branch: 'main'
            }
        }
        stage('Deploy'){
            steps{
                sh "docker compose down && docker compose up -d"
            }
        }
    }
}
