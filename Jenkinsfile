pipeline {

    agent any

    environment {

        IMAGE_NAME = "dheerajkapuganti/docker-demo:v1"

    }

    stages {

        stage('Build Image') {

            steps {

                bat 'docker build -t %IMAGE_NAME% .'

            }

        }

        stage('Push Image') {

            steps {

                withCredentials([
                    usernamePassword(
                        credentialsId: 'dockerhub-creds',
                        usernameVariable: 'DOCKER_USER',
                        passwordVariable: 'DOCKER_PASS'
                    )
                ]) {

                    bat '''
                    echo Username=%DOCKER_USER%
                    '''

                }

            }

        }

    }

}
