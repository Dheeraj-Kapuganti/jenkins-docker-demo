pipeline {

    agent any

    stages {

        stage('Checkout') {

            steps {

                checkout scm

            }

        }

        stage('Build Docker Image') {

            steps {

                bat 'docker build -t docker-demo:v1 .'

            }

        }

    }

}