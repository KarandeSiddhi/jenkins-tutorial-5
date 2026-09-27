pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t tut5 .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker stop containertut5 || exit 0'
                bat 'docker rm containertut5 || exit 0'
                bat 'docker run -d --name containertut5 -p 5000:5000 tut5'
            }
        }
    }
}
